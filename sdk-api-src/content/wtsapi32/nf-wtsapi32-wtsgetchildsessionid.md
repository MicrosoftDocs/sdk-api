---
UID: NF:wtsapi32.WTSGetChildSessionId
title: WTSGetChildSessionId function
author: windows-sdk-content
description: Retrieves the child session identifier, if present.
old-location: termserv\wtsgetchildsessionid.htm
old-project: termserv
ms.assetid: EA78660C-438D-458C-B723-ED1C8AA60FA5
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: WTSGetChildSessionId, WTSGetChildSessionId function [Remote Desktop Services], termserv.wtsgetchildsessionid, wtsapi32/WTSGetChildSessionId
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WTS_VIRTUAL_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wtsapi32.dll
api_name:
 - WTSGetChildSessionId
product: Windows
targetos: Windows
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WTSGetChildSessionId function


## -description


Retrieves the child session identifier, if present.


## -parameters




### -param pSessionId [out]

The address of a <b>ULONG</b> variable that receives the child session identifier. This will be (<b>ULONG</b>)–1 if there is no child session for the current session.


## -returns



Returns nonzero if the function succeeds or zero otherwise.




## -remarks



For more information about child sessions, see <a href="https://msdn.microsoft.com/65B9DB67-4EE8-40B5-B465-CA425792C62B">Child Sessions</a>.



