---
UID: NF:mprapi.MprAdminInterfaceUpdatePhonebookInfo
title: MprAdminInterfaceUpdatePhonebookInfo function (mprapi.h)
description: The MprAdminInterfaceUpdatePhonebookInfo function forces the router to pick up changes made on a specified demand-dial interface. Call this function after changes are made to a phone-book entry for a demand-dial interface.
helpviewer_keywords: ["MprAdminInterfaceUpdatePhonebookInfo","MprAdminInterfaceUpdatePhonebookInfo function [RAS]","_mpr_mpradmininterfaceupdatephonebookinfo","mprapi/MprAdminInterfaceUpdatePhonebookInfo","rras.mpradmininterfaceupdatephonebookinfo"]
old-location: rras\mpradmininterfaceupdatephonebookinfo.htm
tech.root: RRAS
ms.assetid: fa337886-6fae-4e38-a59a-e26036c80d39
ms.date: 12/05/2018
ms.keywords: MprAdminInterfaceUpdatePhonebookInfo, MprAdminInterfaceUpdatePhonebookInfo function [RAS], _mpr_mpradmininterfaceupdatephonebookinfo, mprapi/MprAdminInterfaceUpdatePhonebookInfo, rras.mpradmininterfaceupdatephonebookinfo
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
 - MprAdminInterfaceUpdatePhonebookInfo
 - mprapi/MprAdminInterfaceUpdatePhonebookInfo
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
 - MprAdminInterfaceUpdatePhonebookInfo
---

# MprAdminInterfaceUpdatePhonebookInfo function


## -description

The 
<b>MprAdminInterfaceUpdatePhonebookInfo</b> function forces the router to pick up changes made on a specified demand-dial interface. Call this function after changes are made to a phone-book entry for a demand-dial interface.

## -parameters

### -param hMprServer [in]

Handle to the router on which to execute this call. Obtain the handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>.

### -param hInterface [in]

Handle to a demand-dial interface. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacecreate">MprAdminInterfaceCreate</a>.

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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling application does not have sufficient privileges.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANNOT_LOAD_PHONEBOOK</b></dt>
</dl>
</td>
<td width="60%">
The function could not load the phone book into memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANNOT_OPEN_PHONEBOOK</b></dt>
</dl>
</td>
<td width="60%">
The function could not find the phone-book file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DDM_NOT_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
The Demand Dial Manager (DDM) is not running.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INTERFACE_HAS_NO_DEVICES</b></dt>
</dl>
</td>
<td width="60%">
No device is currently associated with this interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hInterface</i> value is invalid.

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



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacecreate">MprAdminInterfaceCreate</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>



<a href="/windows/desktop/RRAS/router-administration-functions">Router Administration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>