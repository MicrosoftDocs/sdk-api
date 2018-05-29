---
UID: NF:wtsapi32.WTSStopRemoteControlSession
title: WTSStopRemoteControlSession function
author: windows-sdk-content
description: Stops a remote control session.
old-location: termserv\wtsstopremotecontrolsession.htm
old-project: TermServ
ms.assetid: 65e5b584-4ffc-4b89-992e-7ada7df0262b
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: WTSStopRemoteControlSession, WTSStopRemoteControlSession function [Remote Desktop Services], termserv.wtsstopremotecontrolsession, wtsapi32/WTSStopRemoteControlSession
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WTS_VIRTUAL_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wtsapi32.dll
api_name:
-	WTSStopRemoteControlSession
product: Windows
targetos: Windows
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WTSStopRemoteControlSession function


## -description


Stops a remote control session.


## -parameters




### -param LogonId [in]

The logon ID of the session that you want to stop the remote control of.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



