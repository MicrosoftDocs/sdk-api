---
UID: NF:wtsapi32.WTSGetChildSessionId
title: WTSGetChildSessionId function (wtsapi32.h)
description: Retrieves the child session identifier, if present.
helpviewer_keywords: ["WTSGetChildSessionId","WTSGetChildSessionId function [Remote Desktop Services]","termserv.wtsgetchildsessionid","wtsapi32/WTSGetChildSessionId"]
old-location: termserv\wtsgetchildsessionid.htm
tech.root: TermServ
ms.assetid: EA78660C-438D-458C-B723-ED1C8AA60FA5
ms.date: 12/05/2018
ms.keywords: WTSGetChildSessionId, WTSGetChildSessionId function [Remote Desktop Services], termserv.wtsgetchildsessionid, wtsapi32/WTSGetChildSessionId
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
 - WTSGetChildSessionId
 - wtsapi32/WTSGetChildSessionId
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
 - WTSGetChildSessionId
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

For more information about child sessions, see <a href="/windows/desktop/TermServ/child-sessions">Child Sessions</a>.