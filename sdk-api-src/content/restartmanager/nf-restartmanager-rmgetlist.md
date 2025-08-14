---
UID: NF:restartmanager.RmGetList
title: RmGetList function (restartmanager.h)
description: Gets a list of all applications and services that are currently using resources that have been registered with the Restart Manager session.
helpviewer_keywords: ["RmGetList","RmGetList function [Restart Mgr]","restartmanager/RmGetList","rstmgr.rmgetlist"]
old-location: rstmgr\rmgetlist.htm
tech.root: rstmgr
ms.assetid: de4feea4-2b45-4430-a4b3-8ca26c455e42
ms.date: 12/05/2018
ms.keywords: RmGetList, RmGetList function [Restart Mgr], restartmanager/RmGetList, rstmgr.rmgetlist
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
 - RmGetList
 - restartmanager/RmGetList
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
 - RmGetList
---

# RmGetList function


## -description

Gets a list of all applications and services that are currently using resources that have been registered with the Restart Manager session.

## -parameters

### -param dwSessionHandle [in]

A handle to an existing Restart Manager session.

### -param pnProcInfoNeeded [out]

A pointer to an array size necessary to receive <a href="/windows/desktop/api/restartmanager/ns-restartmanager-rm_process_info">RM_PROCESS_INFO</a> structures required to return information for all affected applications and services.

### -param pnProcInfo [in, out]

A pointer to the total number of <a href="/windows/desktop/api/restartmanager/ns-restartmanager-rm_process_info">RM_PROCESS_INFO</a> structures in an array and number of structures filled.

### -param rgAffectedApps [in, out, optional]

An array of <a href="/windows/desktop/api/restartmanager/ns-restartmanager-rm_process_info">RM_PROCESS_INFO</a> structures that list the applications and services  using resources that have been registered with the session.

### -param lpdwRebootReasons [out]

Pointer to location that receives a value of the  <a href="/windows/desktop/api/restartmanager/ne-restartmanager-rm_reboot_reason">RM_REBOOT_REASON</a> enumeration that describes the reason a system restart is needed.

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
<dt><b>ERROR_MORE_DATA</b></dt>
<dt>234</dt>
</dl>
</td>
<td width="60%">
This error value is returned by the <a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmgetlist">RmGetList</a> function if the <i>rgAffectedApps</i> buffer is too small to hold all application information in the list.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANCELLED</b></dt>
<dt>1223</dt>
</dl>
</td>
<td width="60%">
The current operation is canceled by user.

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
<dt><b>ERROR_WRITE_FAULT</b></dt>
<dt>29</dt>
</dl>
</td>
<td width="60%">
An operation was unable to read or write to the registry.

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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
A path registered to the Restart Manager session is a directory.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmcancelcurrenttask">RmCancelCurrentTask</a>
