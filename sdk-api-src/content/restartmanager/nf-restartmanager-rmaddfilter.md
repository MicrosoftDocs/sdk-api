---
UID: NF:restartmanager.RmAddFilter
title: RmAddFilter function (restartmanager.h)
description: Modifies the shutdown or restart actions that are applied to an application or service.
helpviewer_keywords: ["RmAddFilter","RmAddFilter function [Restart Mgr]","restartmanager/RmAddFilter","rstmgr.rmaddfilter"]
old-location: rstmgr\rmaddfilter.htm
tech.root: rstmgr
ms.assetid: 63d1d1d2-d7b7-4d6c-99f9-b849229e171f
ms.date: 12/05/2018
ms.keywords: RmAddFilter, RmAddFilter function [Restart Mgr], restartmanager/RmAddFilter, rstmgr.rmaddfilter
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
 - RmAddFilter
 - restartmanager/RmAddFilter
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
 - RmAddFilter
---

# RmAddFilter function


## -description

Modifies the shutdown or restart actions that are applied to an application or service. The primary installer can call the <b>RmAddFilter</b> function multiple times. The most recent call overrides any previous modifications to the same file, process, or service.

## -parameters

### -param dwSessionHandle [in]

A handle to an existing Restart Manager session.

### -param strModuleName [in, optional]

A pointer to a <b>null</b>-terminated string value that contains the full path to the application's executable file. Modifications to shutdown or restart actions are applied for the application that is referenced by the full path.  This parameter must be <b>NULL</b> if the <i>Application</i> or <i>strServiceShortName</i> parameter is non-<b>NULL</b>.

### -param pProcess [in, optional]

A pointer to a <a href="/windows/desktop/api/restartmanager/ns-restartmanager-rm_unique_process">RM_UNIQUE_PROCESS</a> structure for the application.  Modifications to shutdown or restart actions are applied for the application that is referenced by the <b>RM_UNIQUE_PROCESS</b> structure. This parameter must be <b>NULL</b> if the <i>strFilename</i>  or <i>strShortServiceName</i> parameter is non-<b>NULL</b>.

### -param strServiceShortName [in, optional]

A pointer to a <b>null</b>-terminated string value that contains the short service name. Modifications to shutdown or restart actions are applied for the service that is referenced by short service filename.  This parameter must be <b>NULL</b> if the <i>strFilename</i> or <i>Application</i> parameter is non-<b>NULL</b>.

### -param FilterAction [in]

An <a href="/windows/desktop/api/restartmanager/ne-restartmanager-rm_filter_action">RM_FILTER_ACTION</a> enumeration value that specifies the type of modification to be applied.

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
<dt><b>ERROR_BAD_ARGUMENTS</b></dt>
<dt>160</dt>
</dl>
</td>
<td width="60%">
One or more arguments are not correct. This error value is returned by the Restart Manager function if a <b>NULL</b> pointer or 0 is passed in as a parameter that requires a non-<b>null</b> and non-zero value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SESSION_CREDENTIAL_CONFLICT</b></dt>
<dt> 1219</dt>
</dl>
</td>
<td width="60%">
This error is returned when a secondary installer calls this function. This function is only available to primary installers.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmgetfilterlist">RmGetFilterList</a>