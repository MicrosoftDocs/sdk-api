---
UID: NF:restartmanager.RmCancelCurrentTask
title: RmCancelCurrentTask function (restartmanager.h)
description: Cancels the current RmShutdown or RmRestart operation. This function must be called from the application that has started the session by calling the RmStartSession function.
helpviewer_keywords: ["RmCancelCurrentTask","RmCancelCurrentTask function [Restart Mgr]","restartmanager/RmCancelCurrentTask","rstmgr.rmcancelcurrenttask"]
old-location: rstmgr\rmcancelcurrenttask.htm
tech.root: rstmgr
ms.assetid: 58a9a734-667a-48b0-84e2-8cfd85e918bf
ms.date: 12/05/2018
ms.keywords: RmCancelCurrentTask, RmCancelCurrentTask function [Restart Mgr], restartmanager/RmCancelCurrentTask, rstmgr.rmcancelcurrenttask
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
 - RmCancelCurrentTask
 - restartmanager/RmCancelCurrentTask
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
 - RmCancelCurrentTask
---

# RmCancelCurrentTask function


## -description

Cancels the current  <a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmshutdown">RmShutdown</a> or  <a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmrestart">RmRestart</a> operation.  This function must be called from the application that has started the session by calling the <a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmstartsession">RmStartSession</a> function.

## -parameters

### -param dwSessionHandle [in]

A handle to an existing session.

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
A cancellation of the current operation is requested.

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
No Restart Manager session exists for the handle supplied.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmrestart">RmRestart</a>



<a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmshutdown">RmShutdown</a>