---
UID: NF:wtsapi32.WTSEnableChildSessions
title: WTSEnableChildSessions function
author: windows-sdk-content
description: Enables or disables Child Sessions.
old-location: termserv\wtsenablechildsessions.htm
tech.root: termserv
ms.assetid: BA995C04-9004-4A41-8E4A-8701E8C64F2E
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: WTSEnableChildSessions, WTSEnableChildSessions function [Remote Desktop Services], termserv.wtsenablechildsessions, wtsapi32/WTSEnableChildSessions
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wtsapi32.dll
api_name:
 - WTSEnableChildSessions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WTSEnableChildSessions function


## -description


Enables or disables <a href="https://msdn.microsoft.com/65B9DB67-4EE8-40B5-B465-CA425792C62B">Child Sessions</a>.


## -parameters




### -param bEnable

Indicates whether to enable or disable child sessions. Pass <b>TRUE</b> if child sessions are to be enabled or <b>FALSE</b> otherwise.


## -returns



Returns nonzero if the function succeeds or zero otherwise.




## -remarks



For more information about child sessions, see <a href="https://msdn.microsoft.com/65B9DB67-4EE8-40B5-B465-CA425792C62B">Child Sessions</a>.



