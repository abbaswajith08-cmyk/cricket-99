# cricket-99
import 'dart:math';
import 'dart:io';

void main() {
  int totalRuns = 0;
  int wickets = 0;
  int balls = 6;

  Random random = Random();

  print("🏏 Welcome to Mini Cricket Game");
  print("You have 6 balls and 2 wickets.\n");

  for (int i = 1; i <= balls; i++) {
    if (wickets == 2) {
      print("All Out!");
      break;
    }

    stdout.write("Press Enter to play Ball $i...");
    stdin.readLineSync();

    int result = random.nextInt(7); // 0 to 6

    if (result == 0) {
      wickets++;
      print("❌ OUT! Wickets: $wickets");
    } else {
      totalRuns += result;
      print("🏏 You scored $result run(s)");
    }

    print("Current Score: $totalRuns/$wickets\n");
  }

  print("================================");
  print("🏆 Innings Finished");
  print("Final Score: $totalRuns/$wickets");
}
