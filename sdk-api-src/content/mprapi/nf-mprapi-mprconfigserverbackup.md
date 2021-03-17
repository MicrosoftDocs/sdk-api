---
UID: NF:mprapi.MprConfigServerBackup
title: MprConfigServerBackup function (mprapi.h)
description: The MprConfigServerBackup function creates a backup of the router-manager, interface, and phone-book configuration for the router.
helpviewer_keywords: ["MprConfigServerBackup","MprConfigServerBackup function [RAS]","_mpr_mprconfigserverbackup","mprapi/MprConfigServerBackup","rras.mprconfigserverbackup"]
old-location: rras\mprconfigserverbackup.htm
tech.root: RRAS
ms.assetid: 7e318742-78ba-4eb4-818b-939688e79d54
ms.date: 12/05/2018
ms.keywords: MprConfigServerBackup, MprConfigServerBackup function [RAS], _mpr_mprconfigserverbackup, mprapi/MprConfigServerBackup, rras.mprconfigserverbackup
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MprConfigServerBackup
 - mprapi/MprConfigServerBackup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprConfigServerBackup
---

# MprConfigServerBackup function


## -description

The 
<b>MprConfigServerBackup</b> function creates a backup of the router-manager, interface, and phone-book configuration for the router.

## -parameters

### -param hMprConfig [in]

Handle to the router configuration. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>.

### -param lpwsPath [in]

Pointer to a <b>null</b>-terminated Unicode string that specifies the path to the directory in which to write the backup files. This path should end with a trailing backslash.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>hMprConfig</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient resources to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

</td>
</tr>
</table>
 


<div> </div>

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverrestore">MprConfigServerRestore</a>



<a href="/windows/desktop/RRAS/router-configuration-functions">Router Configuration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>