---
UID: NF:mprapi.MprConfigInterfaceGetCustomInfoEx
title: MprConfigInterfaceGetCustomInfoEx function (mprapi.h)
description: Retrieves the custom IKEv2 policy configuration for the specified interface.
helpviewer_keywords: ["MprConfigInterfaceGetCustomInfoEx","MprConfigInterfaceGetCustomInfoEx function [RAS]","mprapi/MprConfigInterfaceGetCustomInfoEx","rras.mprconfiginterfacegetcustominfoex"]
old-location: rras\mprconfiginterfacegetcustominfoex.htm
tech.root: RRAS
ms.assetid: 97fa62f4-5e1c-4634-a3c7-974425717080
ms.date: 12/05/2018
ms.keywords: MprConfigInterfaceGetCustomInfoEx, MprConfigInterfaceGetCustomInfoEx function [RAS], mprapi/MprConfigInterfaceGetCustomInfoEx, rras.mprconfiginterfacegetcustominfoex
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - MprConfigInterfaceGetCustomInfoEx
 - mprapi/MprConfigInterfaceGetCustomInfoEx
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
 - MprConfigInterfaceGetCustomInfoEx
---

# MprConfigInterfaceGetCustomInfoEx function


## -description

Retrieves the custom IKEv2 policy configuration for the specified interface.

## -parameters

### -param hMprConfig [in]

The handle to the router configuration. This handle is obtained by calling the <a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a> function.

### -param hRouterInterface [in]

The handle to the interface configuration being updated. Obtain this handle by calling the  <a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacecreate">MprConfigInterfaceCreate</a> function, the <a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacegethandle">MprConfigInterfaceGetHandle</a> function, or the <a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfaceenum">MprConfigInterfaceEnum</a> function.

### -param pCustomInfo [out]

A pointer to a <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_if_custominfoex0">MPR_IF_CUSTOMINFOEX</a>  structure. When you have finished using the structure, free the buffer by calling the <a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigbufferfree">MprConfigBufferFree</a> function.

## -returns

If the function succeeds, the return value is <b>NO_ERROR</b>. If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
<li>The <i>hMprConfig</i> parameter is <b>NULL</b>.</li>
<li>The <i>hRouterInterface</i> parameter is <b>NULL</b>.</li>
<li>The <i>pCustomInfo</i> parameter is <b>NULL</b>.</li>
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
There were insufficient resources to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SUCH_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The interface that corresponds to <i>hRouterInterface</i> parameter is not present in the router configuration.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/RRAS/router-configuration-functions">Router Configuration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>