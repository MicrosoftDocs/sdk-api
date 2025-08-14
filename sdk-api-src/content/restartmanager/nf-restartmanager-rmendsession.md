---
UID: NF:restartmanager.RmEndSession
title: RmEndSession function (restartmanager.h)
description: Ends the Restart Manager session.
helpviewer_keywords: ["RmEndSession","RmEndSession function [Restart Mgr]","restartmanager/RmEndSession","rstmgr.rmendsession"]
old-location: rstmgr\rmendsession.htm
tech.root: rstmgr
ms.assetid: 2681cb69-a66f-4aec-a164-98d2d28f9908
ms.date: 12/05/2018
ms.keywords: RmEndSession, RmEndSession function [Restart Mgr], restartmanager/RmEndSession, rstmgr.rmendsession
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
 - RmEndSession
 - restartmanager/RmEndSession
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-base-rstrtmgr-l1-1-0.dll
 - Rstrtmgr.dll
api_name:
 - RmEndSession
---

# RmEndSession function


## -description

Ends the Restart Manager session. This function should be called by the primary installer that has previously started the session by calling the <a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmstartsession">RmStartSession</a> function. The <b>RmEndSession</b> function can be called by a secondary installer that is joined to the session once no more resources need to be registered by the secondary installer.

## -parameters

### -param dwSessionHandle [in]

A handle to an existing Restart Manager session.

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
<dt><b>ERROR_OUTOFMEMORY</b></dt>
<dt>14</dt>
</dl>
</td>
<td width="60%">
A Restart Manager operation could not complete because not enough memory was available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
An invalid handle was passed to the function. No Restart Manager session exists for the handle supplied.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmjoinsession">RmJoinSession</a>



<a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmstartsession">RmStartSession</a>