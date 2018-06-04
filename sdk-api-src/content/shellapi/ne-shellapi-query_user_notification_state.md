---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# QUERY_USER_NOTIFICATION_STATE enumeration


## -description


Specifies the state of the machine for the current user in relation to the propriety of sending a notification. Used by <a href="https://msdn.microsoft.com/da6b3915-f4fe-4bab-9bae-9bff0b97b5a0">SHQueryUserNotificationState</a>.


## -enum-fields




### -field QUNS_NOT_PRESENT

A screen saver is displayed, the machine is locked, or a nonactive Fast User Switching session is in progress.


### -field QUNS_BUSY

A full-screen application is running or Presentation Settings are applied. Presentation Settings allow a user to put their machine into a state fit for an uninterrupted presentation, such as a set of PowerPoint slides, with a single click.


### -field QUNS_RUNNING_D3D_FULL_SCREEN

A full-screen (exclusive mode) Direct3D application is running.


### -field QUNS_PRESENTATION_MODE

The user has activated Windows presentation settings to block notifications and pop-up messages.


### -field QUNS_ACCEPTS_NOTIFICATIONS

None of the other states are found, notifications can be freely sent.


### -field QUNS_QUIET_TIME

<b>Introduced in Windows 7</b>. The current user is in "quiet time", which is the first hour after a new user logs into his or her account for the first time. During this time, most notifications should not be sent or shown. This lets a user become accustomed to a new computer system without those distractions. Quiet time also occurs for each user after an operating system upgrade or clean installation.
        
                        

Applications should set the <a href="https://msdn.microsoft.com/fdcc42c1-b3e5-4b04-8d79-7b6c29699d53">NIIF_RESPECT_QUIET_TIME</a> flag in their notifications or balloon tooltip, which prevents those items from being displayed while the current user is in the quiet-time state.

Note that during quiet time, if the user is in one of the other blocked modes (QUNS_NOT_PRESENT, QUNS_BUSY, QUNS_PRESENTATION_MODE, or QUNS_RUNNING_D3D_FULL_SCREEN) <a href="https://msdn.microsoft.com/da6b3915-f4fe-4bab-9bae-9bff0b97b5a0">SHQueryUserNotificationState</a> returns only that value, and does not report QUNS_QUIET_TIME.


### -field QUNS_APP

<b>Introduced in Windows 8</b>. A Windows Store app is running.

