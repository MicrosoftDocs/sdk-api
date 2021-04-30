---
UID: NF:mprapi.MprConfigInterfaceGetInfo
title: MprConfigInterfaceGetInfo function (mprapi.h)
description: The MprConfigInterfaceGetInfo function retrieves the configuration for the specified interface from the router.
helpviewer_keywords: ["MprConfigInterfaceGetInfo","MprConfigInterfaceGetInfo function [RAS]","_mpr_mprconfiginterfacegetinfo","mprapi/MprConfigInterfaceGetInfo","rras.mprconfiginterfacegetinfo"]
old-location: rras\mprconfiginterfacegetinfo.htm
tech.root: RRAS
ms.assetid: f33f9e66-1668-4839-9c98-5945104110bc
ms.date: 12/05/2018
ms.keywords: MprConfigInterfaceGetInfo, MprConfigInterfaceGetInfo function [RAS], _mpr_mprconfiginterfacegetinfo, mprapi/MprConfigInterfaceGetInfo, rras.mprconfiginterfacegetinfo
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
 - MprConfigInterfaceGetInfo
 - mprapi/MprConfigInterfaceGetInfo
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
 - MprConfigInterfaceGetInfo
---

# MprConfigInterfaceGetInfo function


## -description

The 
<b>MprConfigInterfaceGetInfo</b> function retrieves the configuration for the specified interface from the router.

## -parameters

### -param hMprConfig [in]

Handle to the router configuration. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>.

### -param hRouterInterface [in]

Handle to the interface configuration for which to retrieve information. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacecreate">MprConfigInterfaceCreate</a>, 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacegethandle">MprConfigInterfaceGetHandle</a>, or 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfaceenum">MprConfigInterfaceEnum</a>.

### -param dwLevel [in]

A DWORD value that describes the format in which the information is returned in the <i>lplpBuffer</i> parameter. Acceptable values for <i>dwLevel</i> include 0, 1, 2 and 3, as listed in the following table.

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

### -param lplpBuffer [in, out]

 


On input, a non-<b>NULL</b> pointer. 

On successful completion, a pointer to an array of 
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_0">MPR_INTERFACE_0</a>, 
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_1">MPR_INTERFACE_1</a>,  
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_2">MPR_INTERFACE_2</a>, or  <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_3">MPR_INTERFACE_3</a> structure. The <i>dwLevel</i> parameter indicates the type of structure.
					Free this buffer by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigbufferfree">MprConfigBufferFree</a>.

### -param lpdwBufferSize [out]

Pointer to a <b>DWORD</b> variable. This variable receives the size, in bytes, of the data returned through <i>lplpBuffer</i>.

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
<li><i>hRouterInterface</i> is <b>NULL</b></li>
<li><i>dwLevel</i> is not 0, 1, 2, or 3.</li>
<li><i>lplpBuffer</i> is <b>NULL</b></li>
<li><i>lpdwBufferSize</i> is <b>NULL</b></li>
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
<dt><b>ERROR_NO_SUCH_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The interface that corresponds to <i>hRouterInterface</i> is not present in the router configuration.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigbufferfree">MprConfigBufferFree</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacecreate">MprConfigInterfaceCreate</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfaceenum">MprConfigInterfaceEnum</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacegethandle">MprConfigInterfaceGetHandle</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>



<a href="/windows/desktop/RRAS/router-configuration-functions">Router Configuration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>