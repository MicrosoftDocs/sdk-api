---
UID: NF:restartmanager.RmStartSession
title: RmStartSession function (restartmanager.h)
description: Starts a new Restart Manager session.
helpviewer_keywords: ["RmStartSession","RmStartSession function [Restart Mgr]","restartmanager/RmStartSession","rstmgr.rmstartsession"]
old-location: rstmgr\rmstartsession.htm
tech.root: rstmgr
ms.assetid: bc79c6e5-49e6-44d3-90f6-b0109fb9611b
ms.date: 12/05/2018
ms.keywords: RmStartSession, RmStartSession function [Restart Mgr], restartmanager/RmStartSession, rstmgr.rmstartsession
req.header: restartmanager.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rstrtmgr.lib
req.dll: Rstrtmgr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RmStartSession
 - restartmanager/RmStartSession
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rstrtmgr.dll
api_name:
 - RmStartSession
---

# RmStartSession function


## -description

Starts a new Restart Manager session. A maximum of 64 Restart Manager sessions per user session can be open on the system at the same time.   When this function starts a session, it returns a session handle and session key that can be used in subsequent calls to the Restart Manager API.

## -parameters

### -param pSessionHandle [out]

A pointer to the handle of a Restart Manager session. The session handle can be passed in subsequent calls to the Restart Manager API.

### -param dwSessionFlags

Reserved. This parameter should be 0.

### -param strSessionKey [out]

A <b>null</b>-terminated string that contains the session key to the new session. The string of size `CCH_RM_SESSION_KEY + 1` must be allocated before calling the <b>RmStartSession</b> function.

## -returns

This is the most recent error received. The function can return one of the <a href="/windows/desktop/Debug/system-error-codes">system error codes</a> that are defined in Winerror.h. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The function completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SEM_TIMEOUT</b></dt>
<dt>121</dt>
</dl>
</td>
<td width="60%">
A Restart Manager function could not obtain a Registry write mutex in the allotted time. A system restart is recommended because further use of the Restart Manager is likely to fail.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_ARGUMENTS</b></dt>
<dt>160</dt>
</dl>
</td>
<td width="60%">
One or more arguments are not correct. This error value is returned by the Restart Manager function if a <b>NULL</b> pointer or 0 is passed in a parameter that requires a non-<b>null</b> and non-zero value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MAX_SESSIONS_REACHED</b></dt>
<dt>353</dt>
</dl>
</td>
<td width="60%">
The maximum number of sessions has been reached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WRITE_FAULT</b></dt>
<dt>29</dt>
</dl>
</td>
<td width="60%">
The system cannot write to the specified device.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OUTOFMEMORY</b></dt>
<dt>14</dt>
</dl>
</td>
<td width="60%">
A Restart Manager operation could not complete because not enough memory was available.

</td>
</tr>
</table>

## -remarks

The <b>RmStartSession</b> function returns an error if a session with the same session key already exists.

The <b>RmStartSession</b> function should be called by the primary installer that controls the user interface or that controls the installation sequence of multiple patches in an update.

A secondary installer can join an existing Restart Manager session by calling the <a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmjoinsession">RmJoinSession</a> function with the session handle and session key returned from the <b>RmStartSession</b> function call of the primary installer.

## -see-also

<a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmendsession">RmEndSession</a>



<a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmjoinsession">RmJoinSession</a>
