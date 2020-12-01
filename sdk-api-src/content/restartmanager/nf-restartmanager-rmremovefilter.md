---
UID: NF:restartmanager.RmRemoveFilter
title: RmRemoveFilter function (restartmanager.h)
description: Removes any modifications to shutdown or restart actions that have been applied using the RmAddFilter function.
helpviewer_keywords: ["RmRemoveFilter","RmRemoveFilter function [Restart Mgr]","restartmanager/RmRemoveFilter","rstmgr.rmremovefilter"]
old-location: rstmgr\rmremovefilter.htm
tech.root: rstmgr
ms.assetid: fb1baa7b-0dfb-4bd1-8a3f-cfaf9bf4079f
ms.date: 12/05/2018
ms.keywords: RmRemoveFilter, RmRemoveFilter function [Restart Mgr], restartmanager/RmRemoveFilter, rstmgr.rmremovefilter
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
 - RmRemoveFilter
 - restartmanager/RmRemoveFilter
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
 - RmRemoveFilter
---

# RmRemoveFilter function


## -description

Removes any modifications to shutdown or restart actions that have been applied using the <a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmaddfilter">RmAddFilter</a> function. The primary installer can call  the <b>RmRemoveFilter</b> function multiple times.

## -parameters

### -param dwSessionHandle [in]

A handle to an existing Restart Manager session.

### -param strModuleName [in, optional]

A pointer to a <b>null</b>-terminated string value that contains the full path for the application's  executable file. The <b>RmRemoveFilter</b> function removes any modifications to the referenced application's shutdown or restart actions previously applied by the <a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmaddfilter">RmAddFilter</a> function.  This parameter must be <b>NULL</b> if the <i>Application</i> or <i>strServiceShortName</i> parameter is non-<b>NULL</b>.

### -param pProcess [in, optional]

The <a href="/windows/desktop/api/restartmanager/ns-restartmanager-rm_unique_process">RM_UNIQUE_PROCESS</a> structure for the application. The <b>RmRemoveFilter</b> function removes any modifications to the referenced application's shutdown or restart actions previously applied by the <a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmaddfilter">RmAddFilter</a> function.  This parameter must be <b>NULL</b> if the <i>strFilename</i>  or <i>strShortServiceName</i> parameter is non-<b>NULL</b>.

### -param strServiceShortName [in, optional]

A pointer to a <b>null</b>-terminated string value that contains the short service name.  The <b>RmRemoveFilter</b> function removes any modifications to the referenced service's shutdown or restart actions previously applied by the <a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmaddfilter">RmAddFilter</a> function.  This parameter must be <b>NULL</b> if the <i>strFilename</i> or <i>Application</i> parameter is non-<b>NULL</b>.

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
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The specified filter could not be found.

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