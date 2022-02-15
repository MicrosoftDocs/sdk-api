---
UID: NE:shellapi.__unnamed_enum_0
title: QUERY_USER_NOTIFICATION_STATE (shellapi.h)
description: Specifies the state of the machine for the current user in relation to the propriety of sending a notification. Used by SHQueryUserNotificationState.
helpviewer_keywords: ["QUERY_USER_NOTIFICATION_STATE","QUERY_USER_NOTIFICATION_STATE enumeration [Windows Shell]","QUNS_ACCEPTS_NOTIFICATIONS","QUNS_APP","QUNS_BUSY","QUNS_NOT_PRESENT","QUNS_PRESENTATION_MODE","QUNS_QUIET_TIME","QUNS_RUNNING_D3D_FULL_SCREEN","_shell_QUERY_USER_NOTIFICATION_STATE","shell.QUERY_USER_NOTIFICATION_STATE","shellapi/QUERY_USER_NOTIFICATION_STATE","shellapi/QUNS_ACCEPTS_NOTIFICATIONS","shellapi/QUNS_APP","shellapi/QUNS_BUSY","shellapi/QUNS_NOT_PRESENT","shellapi/QUNS_PRESENTATION_MODE","shellapi/QUNS_QUIET_TIME","shellapi/QUNS_RUNNING_D3D_FULL_SCREEN"]
old-location: shell\QUERY_USER_NOTIFICATION_STATE.htm
tech.root: shell
ms.assetid: b26439dd-6695-45d8-8c7f-5bbd5eaf5b54
ms.date: 12/05/2018
ms.keywords: QUERY_USER_NOTIFICATION_STATE, QUERY_USER_NOTIFICATION_STATE enumeration [Windows Shell], QUNS_ACCEPTS_NOTIFICATIONS, QUNS_APP, QUNS_BUSY, QUNS_NOT_PRESENT, QUNS_PRESENTATION_MODE, QUNS_QUIET_TIME, QUNS_RUNNING_D3D_FULL_SCREEN, _shell_QUERY_USER_NOTIFICATION_STATE, shell.QUERY_USER_NOTIFICATION_STATE, shellapi/QUERY_USER_NOTIFICATION_STATE, shellapi/QUNS_ACCEPTS_NOTIFICATIONS, shellapi/QUNS_APP, shellapi/QUNS_BUSY, shellapi/QUNS_NOT_PRESENT, shellapi/QUNS_PRESENTATION_MODE, shellapi/QUNS_QUIET_TIME, shellapi/QUNS_RUNNING_D3D_FULL_SCREEN
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: QUERY_USER_NOTIFICATION_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - QUERY_USER_NOTIFICATION_STATE
 - shellapi/QUERY_USER_NOTIFICATION_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shellapi.h
api_name:
 - QUERY_USER_NOTIFICATION_STATE
---

# QUERY_USER_NOTIFICATION_STATE enumeration


## -description

Specifies the state of the machine for the current user in relation to the propriety of sending a notification. Used by <a href="/windows/desktop/api/shellapi/nf-shellapi-shqueryusernotificationstate">SHQueryUserNotificationState</a>.

## -enum-fields

### -field QUNS_NOT_PRESENT:1

A screen saver is displayed, the machine is locked, or a nonactive Fast User Switching session is in progress.

### -field QUNS_BUSY:2

A full-screen application is running or Presentation Settings are applied. Presentation Settings allow a user to put their machine into a state fit for an uninterrupted presentation, such as a set of PowerPoint slides, with a single click.

### -field QUNS_RUNNING_D3D_FULL_SCREEN:3

A full-screen (exclusive mode) Direct3D application is running.

### -field QUNS_PRESENTATION_MODE:4

The user has activated Windows presentation settings to block notifications and pop-up messages.

### -field QUNS_ACCEPTS_NOTIFICATIONS:5

None of the other states are found, notifications can be freely sent.

### -field QUNS_QUIET_TIME:6

<b>Introduced in Windows 7</b>. The current user is in "quiet time", which is the first hour after a new user logs into his or her account for the first time. During this time, most notifications should not be sent or shown. This lets a user become accustomed to a new computer system without those distractions. Quiet time also occurs for each user after an operating system upgrade or clean installation.
        
                        

Applications should set the <a href="/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa">NIIF_RESPECT_QUIET_TIME</a> flag in their notifications or balloon tooltip, which prevents those items from being displayed while the current user is in the quiet-time state.

Note that during quiet time, if the user is in one of the other blocked modes (QUNS_NOT_PRESENT, QUNS_BUSY, QUNS_PRESENTATION_MODE, or QUNS_RUNNING_D3D_FULL_SCREEN) <a href="/windows/desktop/api/shellapi/nf-shellapi-shqueryusernotificationstate">SHQueryUserNotificationState</a> returns only that value, and does not report QUNS_QUIET_TIME.

### -field QUNS_APP:7

<b>Introduced in Windows 8</b>. A Windows Store app is running.
