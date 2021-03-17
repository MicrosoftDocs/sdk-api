---
UID: NF:wtsapi32.WTSIsChildSessionsEnabled
title: WTSIsChildSessionsEnabled function (wtsapi32.h)
description: Determines whether child sessions are enabled.
helpviewer_keywords: ["WTSIsChildSessionsEnabled","WTSIsChildSessionsEnabled function [Remote Desktop Services]","termserv.wtsischildsessionsenabled","wtsapi32/WTSIsChildSessionsEnabled"]
old-location: termserv\wtsischildsessionsenabled.htm
tech.root: TermServ
ms.assetid: 814828A8-1FFB-4ED2-A695-11C87723D5BB
ms.date: 12/05/2018
ms.keywords: WTSIsChildSessionsEnabled, WTSIsChildSessionsEnabled function [Remote Desktop Services], termserv.wtsischildsessionsenabled, wtsapi32/WTSIsChildSessionsEnabled
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WTSIsChildSessionsEnabled
 - wtsapi32/WTSIsChildSessionsEnabled
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wtsapi32.dll
api_name:
 - WTSIsChildSessionsEnabled
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

For more information about child sessions, see <a href="/windows/desktop/TermServ/child-sessions">Child Sessions</a>.