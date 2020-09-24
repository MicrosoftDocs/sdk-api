---
UID: NF:mprapi.MprAdminInterfaceCreate
title: MprAdminInterfaceCreate function (mprapi.h)
description: The MprAdminInterfaceCreate function creates an interface on a specified server.
helpviewer_keywords: ["MprAdminInterfaceCreate","MprAdminInterfaceCreate function [RAS]","_mpr_mpradmininterfacecreate","mprapi/MprAdminInterfaceCreate","rras.mpradmininterfacecreate"]
old-location: rras\mpradmininterfacecreate.htm
tech.root: RRAS
ms.assetid: c9590ebe-7e49-4ad1-bd9b-0d9c51938bc4
ms.date: 12/05/2018
ms.keywords: MprAdminInterfaceCreate, MprAdminInterfaceCreate function [RAS], _mpr_mpradmininterfacecreate, mprapi/MprAdminInterfaceCreate, rras.mpradmininterfacecreate
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
 - MprAdminInterfaceCreate
 - mprapi/MprAdminInterfaceCreate
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
 - MprAdminInterfaceCreate
---

# MprAdminInterfaceCreate function


## -description

The 
<b>MprAdminInterfaceCreate</b> function creates an interface on a specified server.

## -parameters

### -param hMprServer [in]

Handle to the  router on which to execute this call. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>.

### -param dwLevel [in]

A DWORD value that describes the format in which the information is structured in the <i>lpBuffer</i> parameter. Acceptable values for <i>dwLevel</i> include 0, 1, 2, and 3, as listed in the following table.

<table>
<tr>
<th>Value</th>
<th>Structure Format</th>
</tr>
<tr>
<td>0</td>
<td>
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_0">MPR_INTERFACE_0</a>
</td>
</tr>
<tr>
<td>1</td>
<td>
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_1">MPR_INTERFACE_1</a>
</td>
</tr>
<tr>
<td>2</td>
<td>
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_2">MPR_INTERFACE_2</a>
</td>
</tr>
<tr>
<td>3</td>
<td>Windows Server 2008 or later: <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_3">MPR_INTERFACE_3</a>
</td>
</tr>
</table>

### -param lpbBuffer [in]

A pointer to a 
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_0">MPR_INTERFACE_0</a>, 
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_1">MPR_INTERFACE_1</a>,  
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_2">MPR_INTERFACE_2</a>, or  <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_3">MPR_INTERFACE_3</a> structure. The <i>dwLevel</i> parameter indicates the type of structure.

### -param phInterface [out]

Pointer to a <b>HANDLE</b> variable. The variable receives a handle to use in all subsequent calls to manage this interface.

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
<dt><b>ERROR_DDM_NOT_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
The router interface type  is not supported because the Dynamic Interface Manager is configured to run only on a LAN.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INTERFACE_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
An interface with the same name already exists.

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
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwLevel</i> value is invalid.

</td>
</tr>
</table>

## -remarks

The 
<b>MprAdminInterfaceCreate</b> function supports the 
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_2">MPR_INTERFACE_2</a> structure. However, 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacecreate">MprConfigInterfaceCreate</a> does not. In order to create a demand-dial interface that is persistent after a reboot, call 
<b>MprAdminInterfaceCreate</b> with 
<b>MPR_INTERFACE_2</b>, then call 
<b>MprConfigInterfaceCreate</b> with 
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_0">MPR_INTERFACE_0</a> or 
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_1">MPR_INTERFACE_1</a>.

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_0">MPR_INTERFACE_0</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_1">MPR_INTERFACE_1</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_2">MPR_INTERFACE_2</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_3">MPR_INTERFACE_3</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacedelete">MprAdminInterfaceDelete</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>



<a href="/windows/desktop/RRAS/router-administration-functions">Router Administration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>