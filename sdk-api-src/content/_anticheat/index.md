---
UID: TP:anticheat
ms.assetid: 730a87ac-451f-39ae-a0e0-c20a9676d363
ms.author: windowsdriverdev
ms.date: 05/07/18
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: portal
---

# TruePlay



Overview of the TruePlay technology.

To develop TruePlay, you need these headers:

 * [gamemonitor.h](..\gamemonitor\index.md)

For the programming guide, see [TruePlay](https://review.docs.microsoft.com/en-us/win32-test/anticheat).

## Functions

| Title   | Description   |
| ---- |:---- |
| [EnableActiveGameMonitoring function](..\gamemonitor\nf-gamemonitor-enableactivegamemonitoring.md) | Enables or disables active monitoring by TruePlay. Use this API to inform TruePlay’s game monitoring that your game is entering a session or experience which does or does not require active monitoring. |
| [GetGameMonitoringPermissionState function](..\gamemonitor\nf-gamemonitor-getgamemonitoringpermissionstate.md) | Gets the current game monitoring permission state of the device. |
| [ReportGameActivity function](..\gamemonitor\nf-gamemonitor-reportgameactivity.md) | Triggers a challenge to the local system that the TruePlay system is active. |
| [SetGameActivityCorrelationId function](..\gamemonitor\nf-gamemonitor-setgameactivitycorrelationid.md) | Allows the game to set a correlation ID that you can use to correlate the game monitoring logs with your own gaming session logs. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [GAME_MONITORING_PERMISSION_STATE enumeration](..\gamemonitor\ne-gamemonitor-game_monitoring_permission_state.md) | Indicates whether game monitoring is disabled. |
