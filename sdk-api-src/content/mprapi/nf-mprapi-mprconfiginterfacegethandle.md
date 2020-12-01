---
UID: NF:mprapi.MprConfigInterfaceGetHandle
title: MprConfigInterfaceGetHandle function (mprapi.h)
description: The MprConfigInterfaceGetHandle function retrieves a handle to the specified interface's configuration in the specified router configuration.
helpviewer_keywords: ["MprConfigInterfaceGetHandle","MprConfigInterfaceGetHandle function [RAS]","_mpr_mprconfiginterfacegethandle","mprapi/MprConfigInterfaceGetHandle","rras.mprconfiginterfacegethandle"]
old-location: rras\mprconfiginterfacegethandle.htm
tech.root: RRAS
ms.assetid: 1088e587-4446-4463-b411-a11e34adaf6a
ms.date: 12/05/2018
ms.keywords: MprConfigInterfaceGetHandle, MprConfigInterfaceGetHandle function [RAS], _mpr_mprconfiginterfacegethandle, mprapi/MprConfigInterfaceGetHandle, rras.mprconfiginterfacegethandle
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
 - MprConfigInterfaceGetHandle
 - mprapi/MprConfigInterfaceGetHandle
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
 - MprConfigInterfaceGetHandle
---

# MprConfigInterfaceGetHandle function


## -description

The 
<b>MprConfigInterfaceGetHandle</b> function retrieves a handle to the specified interface's configuration in the specified router configuration.

## -parameters

### -param hMprConfig [in]

Handle to the router configuration. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>.

### -param lpwsInterfaceName [in]

Pointer to a <b>null</b>-terminated Unicode string that specifies the name of the interface for which the configuration handle is requested. Use the interface GUID as the name of a LAN interface.

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
The <i>hMprConfig</i> parameter is <b>NULL</b>, or the <i>lpwsInterfaceName</i> parameter is <b>NULL</b>, or both parameters are <b>NULL</b>.

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
The specified interface was not found in the router configuration.

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



<a href="/windows/desktop/RRAS/router-configuration-functions">Router Configuration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>