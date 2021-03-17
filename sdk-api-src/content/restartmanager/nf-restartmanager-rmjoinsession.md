---
UID: NF:restartmanager.RmJoinSession
title: RmJoinSession function (restartmanager.h)
description: Joins a secondary installer to an existing Restart Manager session.
helpviewer_keywords: ["RmJoinSession","RmJoinSession function [Restart Mgr]","restartmanager/RmJoinSession","rstmgr.rmjoinsession"]
old-location: rstmgr\rmjoinsession.htm
tech.root: rstmgr
ms.assetid: f9cb2d81-a2bc-4bb7-920a-1630354ea942
ms.date: 12/05/2018
ms.keywords: RmJoinSession, RmJoinSession function [Restart Mgr], restartmanager/RmJoinSession, rstmgr.rmjoinsession
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
 - RmJoinSession
 - restartmanager/RmJoinSession
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
 - RmJoinSession
---

# RmJoinSession function


## -description

Joins a secondary installer to an existing Restart Manager session. This function must be called with a session key that can only be obtained from the primary installer that started the session. A valid session key is required to use any of the Restart Manager functions. After a secondary installer joins a session, it can call the  <a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmregisterresources">RmRegisterResources</a> function to register resources.

## -parameters

### -param pSessionHandle [out]

A pointer to the handle of an existing Restart Manager Session.

### -param strSessionKey [in]

A <b>null</b>-terminated string that contains the session key of an existing session.

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
<dt><b>ERROR_SESSION_CREDENTIAL_CONFLICT</b></dt>
<dt>1219</dt>
</dl>
</td>
<td width="60%">
The session key cannot be validated.

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
<dt>22</dt>
</dl>
</td>
<td width="60%">
One or more arguments are not correct. This error value is returned by the Restart Manager function if a <b>NULL</b> pointer or 0 is passed in a parameter that requires a non-<b>null</b> and non-zero value.

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
An operation was unable  to read or write to the registry.

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

The <b>RmJoinSession</b> function joins a secondary installer to an existing Restart Manager session. This is typically an installer that does not control the user interface and can run either in-process or out-of-process of the primary installer. Only the primary installer can call the <a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmstartsession">RmStartSession</a> function and this is typically the application that controls the user interface or that controls the installation sequence of multiple patches in an update.

## -see-also

<a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmendsession">RmEndSession</a>



<a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmstartsession">RmStartSession</a>