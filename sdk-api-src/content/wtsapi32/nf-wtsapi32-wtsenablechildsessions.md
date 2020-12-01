---
UID: NF:wtsapi32.WTSEnableChildSessions
title: WTSEnableChildSessions function (wtsapi32.h)
description: Enables or disables Child Sessions.
helpviewer_keywords: ["WTSEnableChildSessions","WTSEnableChildSessions function [Remote Desktop Services]","termserv.wtsenablechildsessions","wtsapi32/WTSEnableChildSessions"]
old-location: termserv\wtsenablechildsessions.htm
tech.root: TermServ
ms.assetid: BA995C04-9004-4A41-8E4A-8701E8C64F2E
ms.date: 12/05/2018
ms.keywords: WTSEnableChildSessions, WTSEnableChildSessions function [Remote Desktop Services], termserv.wtsenablechildsessions, wtsapi32/WTSEnableChildSessions
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
 - WTSEnableChildSessions
 - wtsapi32/WTSEnableChildSessions
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
 - WTSEnableChildSessions
---

# WTSEnableChildSessions function


## -description

Enables or disables <a href="/windows/desktop/TermServ/child-sessions">Child Sessions</a>.

## -parameters

### -param bEnable

Indicates whether to enable or disable child sessions. Pass <b>TRUE</b> if child sessions are to be enabled or <b>FALSE</b> otherwise.

## -returns

Returns nonzero if the function succeeds or zero otherwise.

## -remarks

For more information about child sessions, see <a href="/windows/desktop/TermServ/child-sessions">Child Sessions</a>.