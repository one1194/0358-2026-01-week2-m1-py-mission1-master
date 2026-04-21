manager_name = ""
team_budget = 0.0
scout_count = 0 
player_name = ""
over = 0.0
player_stats = []

print("=" * 30)
print("⚽ 방구석 명장 스카우트 시스템 ⚽")
print("=" * 30)

manager_name = input("감독님의 이름을 입력하세요 : ")
team_budge = float(input("구단 초기 예산을 입력하세요(ex : 100.5억) : "))
scout_count = int(input("평가할 능력치 개수를 입력하세요(최소 3이상) : "))

print(f"\n환영합니다, {manager_name}감독님!")
print(f"현재 구단 예산은 {team_budget}억 원이며, 선수당{scout_count}개의 스텟을 평가합니다.\n")

plyer_name = input("스카우트할 선수의 이름을 입력하세요 : ")

start_names = ["슈팅","패스","스피드","피지컬","수비","민첩성"]

print(f"--- {player_name}선수의 능력치 입력 ---")

for i in range(scout_count) : 
 start_val = int(input(f"{start_names[i % 6]} 능력치를 입력하세요 (1~100) : "))
 player_stats.append(stat_val)

stat_total = sum(player_stats)
best_stat = max(splayer_stats)
registered_count = lent(player_stats)

over = stat_total / registered_count 

scout_cost = 0.5
team_budget -= scout_cost

print("\n" + "=" * 30)
print(f"📋 {player_name} 선수의 스카우트 리포트")
print(f"- 입력된 스탯 수 : {registered_count}개")
print(f"- 최고 능력치 : {best_stat}")
print(f"- 종합 능력치(OVR): {over.1f}")
print("=" * 30)

print("▶ 등급 판정: ", end = "")
if ovr >= 90 : 
 print("S등급 (월드클래스)")
elif ovr >= 80 : 
 print("A등급 (즉시 전력감)")
elif ovr >= 70 :
 print("B등급 (유망주)")
else :
 pinrt("C등급 (영입 보류)")

if best_stat >= 90 and ovr < 80 :
 print("▶ 스카우터 코맨트 : 능력치 불균형이 심하지만 확실한 무기가 있습니다. ")

transfer_fee = float(input(f"\n{player_name} 선수의 요구 이적료를 입력하세요 (실수형): "))

print("\n--- 최종 영입 심사 ---")

if transfer_fee <= team_budget : 
 if ovr >= 75 :
  print(f"✅ 영입 성공! {player_name} 선수가 팀에 합류합니다. ")
  team_budget -= transfer_fee 
 else : 
   print("❌ 영입 실패 : 예산은 충분하지만 실력이 기준치에 미달합니다.")
else : 
 print("❌ 영입 실패 : 구단 예산이 부족합니다.")

print(f"\n[잔여 예산] : {team_budget : .1f}억 원")