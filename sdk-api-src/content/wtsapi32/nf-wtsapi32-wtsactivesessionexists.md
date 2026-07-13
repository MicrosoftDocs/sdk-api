---
UID: NF:wtsapi32.WTSActiveSessionExists
tech.root: TermServ
title: WTSActiveSessionExists
ms.date: 09/25/2025
targetos: Windows
description: Returns if there is an active session on the system. 
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: wtsapi32.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows, version 26100
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - Wtsapi32.dll
api_name:
 - WTSActiveSessionExists
f1_keywords:
 - WTSActiveSessionExists
 - wtsapi32/WTSActiveSessionExists
dev_langs:
 - c++
helpviewer_keywords:
 - WTSActiveSessionExists
---

## -description

Returns if there is an active session on the system without enumerating through the list of sessions. It also does not obtain any extra information from Local Session Manager.

## -parameters

### -param pbActiveSessionExists [out]

A pointer to a boolean value indicating whether an active session exists.

## -returns

Returns zero if this function fails. If this function succeeds, a nonzero value is returned.

## -remarks

This function only determines if an active session exists. To get a list of sessions and their states, use `WTSEnumerateSessions`. Many processes running in session 0 use **[WTSEnumerateSessions](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa)** to check if an active session exists, or to do things if an active session exists (ie: get user name, session id, etc). Using **WTSEnumerateSessions** when there are no active sessions is expensive because the entire list of inactive sessions must be enumerated.
