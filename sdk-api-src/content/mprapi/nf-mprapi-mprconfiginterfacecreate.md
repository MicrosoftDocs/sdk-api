---
UID: NF:mprapi.MprConfigInterfaceCreate
title: MprConfigInterfaceCreate function (mprapi.h)
description: The MprConfigInterfaceCreate function creates a router interface in the specified router configuration.
helpviewer_keywords: ["MprConfigInterfaceCreate","MprConfigInterfaceCreate function [RAS]","_mpr_mprconfiginterfacecreate","mprapi/MprConfigInterfaceCreate","rras.mprconfiginterfacecreate"]
old-location: rras\mprconfiginterfacecreate.htm
tech.root: RRAS
ms.assetid: e368aa3c-bb80-49ed-a1da-39777dada960
ms.date: 12/05/2018
ms.keywords: MprConfigInterfaceCreate, MprConfigInterfaceCreate function [RAS], _mpr_mprconfiginterfacecreate, mprapi/MprConfigInterfaceCreate, rras.mprconfiginterfacecreate
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
 - MprConfigInterfaceCreate
 - mprapi/MprConfigInterfaceCreate
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
 - MprConfigInterfaceCreate
---

# MprConfigInterfaceCreate function


## -description

The 
<b>MprConfigInterfaceCreate</b> function creates a router interface in the specified router configuration.

## -parameters

### -param hMprConfig [in]

Handle to the router configuration. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>.

### -param dwLevel [in]

A DWORD value that describes the format in which the information is structured in the <i>lpbBuffer</i> parameter. Acceptable values for <i>dwLevel</i> include 0, 1, 2, and 3, as listed in the following table.

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

A pointer  to a 
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_0">MPR_INTERFACE_0</a>, 
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_1">MPR_INTERFACE_1</a>,  
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_2">MPR_INTERFACE_2</a>, or  <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_3">MPR_INTERFACE_3</a> structure. The <i>dwLevel</i> parameter indicates the type of structure.

### -param phRouterInterface [out]

Pointer to a handle variable. This variable receives a handle to the interface configuration.

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
At least one of the following is true: 




<ul>
<li><i>hMprConfig</i> is <b>NULL</b></li>
<li><i>dwLevel</i> is not 0, 1, 2, or 3.</li>
<li><i>lpbBuffer</i> is <b>NULL</b></li>
<li><i>phRouterInterface</i> is <b>NULL</b></li>
</ul>
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

## -remarks

The 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacecreate">MprAdminInterfaceCreate</a> function supports the 
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_2">MPR_INTERFACE_2</a> structure. However, 
<b>MprConfigInterfaceCreate</b> does not. In order to create a demand-dial interface that is persistent after a reboot, call 
<b>MprAdminInterfaceCreate</b> with 
<b>MPR_INTERFACE_2</b>, then call 
<b>MprConfigInterfaceCreate</b> with 
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_0">MPR_INTERFACE_0</a> or 
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_1">MPR_INTERFACE_1</a>.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacedelete">MprConfigInterfaceDelete</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>



<a href="/windows/desktop/RRAS/router-configuration-functions">Router Configuration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>