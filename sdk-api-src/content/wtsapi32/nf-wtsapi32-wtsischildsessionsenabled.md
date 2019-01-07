---
UID: NF:wtsapi32.WTSIsChildSessionsEnabled
title: WTSIsChildSessionsEnabled function
author: windows-sdk-content
description: Determines whether child sessions are enabled.
old-location: termserv\wtsischildsessionsenabled.htm
tech.root: termserv
ms.assetid: 814828A8-1FFB-4ED2-A695-11C87723D5BB
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WTSIsChildSessionsEnabled, WTSIsChildSessionsEnabled function [Remote Desktop Services], termserv.wtsischildsessionsenabled, wtsapi32/WTSIsChildSessionsEnabled
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
 - WTSIsChildSessionsEnabled
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WTSIsChildSessionsEnabled function


## -description


Determines whether child sessions are enabled.


## -parameters




### -param pbEnabled [out]

The address of a <b>BOOL</b> variable that receives a nonzero value if child sessions are enabled or zero otherwise.


## -returns



Returns nonzero if the function succeeds or zero otherwise.




## -remarks



For more information about child sessions, see <a href="https://msdn.microsoft.com/65B9DB67-4EE8-40B5-B465-CA425792C62B">Child Sessions</a>.



