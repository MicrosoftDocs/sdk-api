---
UID: NF:mprapi.MprConfigInterfaceSetCustomInfoEx
title: MprConfigInterfaceSetCustomInfoEx function (mprapi.h)
description: Sets the custom IKEv2 policy configuration for the specified interface.
helpviewer_keywords: ["MprConfigInterfaceSetCustomInfoEx","MprConfigInterfaceSetCustomInfoEx function [RAS]","mprapi/MprConfigInterfaceSetCustomInfoEx","rras.mprconfiginterfacesetcustominfoex"]
old-location: rras\mprconfiginterfacesetcustominfoex.htm
tech.root: RRAS
ms.assetid: fff18156-ba94-45b7-86c2-a604823a9b08
ms.date: 12/05/2018
ms.keywords: MprConfigInterfaceSetCustomInfoEx, MprConfigInterfaceSetCustomInfoEx function [RAS], mprapi/MprConfigInterfaceSetCustomInfoEx, rras.mprconfiginterfacesetcustominfoex
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
 - MprConfigInterfaceSetCustomInfoEx
 - mprapi/MprConfigInterfaceSetCustomInfoEx
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
 - MprConfigInterfaceSetCustomInfoEx
---

# MprConfigInterfaceSetCustomInfoEx function


## -description

Sets the custom IKEv2 policy configuration for the specified interface.

## -parameters

### -param hMprConfig [in]

The handle to the router configuration. Obtain this handle by calling the <a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a> function.

### -param hRouterInterface [in]

The handle to the interface configuration being updated. Obtain this handle by calling the <a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacecreate">MprConfigInterfaceCreate</a> function, the <a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacegethandle">MprConfigInterfaceGetHandle</a> function, or the <a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfaceenum">MprConfigInterfaceEnum</a> function.

### -param pCustomInfo [in]

A pointer to a <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_if_custominfoex0">MPR_IF_CUSTOMINFOEX</a>  structure.

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
<li>The interface type is not <b>ROUTER_IF_TYPE_FULL_ROUTER</b>.</li>
</ul>
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

<a href="/windows/desktop/RRAS/router-configuration-functions">Router Configuration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>