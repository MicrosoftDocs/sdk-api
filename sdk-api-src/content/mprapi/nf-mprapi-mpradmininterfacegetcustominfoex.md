---
UID: NF:mprapi.MprAdminInterfaceGetCustomInfoEx
title: MprAdminInterfaceGetCustomInfoEx function (mprapi.h)
description: Retrieves tunnel-specific configuration for a specified demand dial interface on a specified server.
helpviewer_keywords: ["MprAdminInterfaceGetCustomInfoEx","MprAdminInterfaceGetCustomInfoEx function [RAS]","mprapi/MprAdminInterfaceGetCustomInfoEx","rras.mpradmininterfacegetcustominfoex"]
old-location: rras\mpradmininterfacegetcustominfoex.htm
tech.root: RRAS
ms.assetid: 01974ac8-dffc-4564-bac1-68ac0437d22b
ms.date: 12/05/2018
ms.keywords: MprAdminInterfaceGetCustomInfoEx, MprAdminInterfaceGetCustomInfoEx function [RAS], mprapi/MprAdminInterfaceGetCustomInfoEx, rras.mpradmininterfacegetcustominfoex
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
 - MprAdminInterfaceGetCustomInfoEx
 - mprapi/MprAdminInterfaceGetCustomInfoEx
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
 - MprAdminInterfaceGetCustomInfoEx
---

# MprAdminInterfaceGetCustomInfoEx function


## -description

Retrieves tunnel-specific configuration for a specified demand dial interface on a specified server.

## -parameters

### -param hMprServer [in]

A handle to the router to query. This handle is obtained by a previous call to the <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a> function.

### -param hInterface [in]

A handle to the interface. This handle is obtained by a previous call to the <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacecreate">MprAdminInterfaceCreate</a> function.

### -param pCustomInfo [out]

A pointer to a <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_if_custominfoex0">MPR_IF_CUSTOMINFOEX</a>  structure. When you have finished using the structure, free the memory by calling the  <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminbufferfree">MprAdminBufferFree</a> function.

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
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hInterface</i> value is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>hInterface</i> value is not valid or if the interface type is not <b>ROUTER_IF_TYPE_FULL_ROUTER</b>.

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
</table>

## -see-also

<a href="/windows/desktop/RRAS/router-administration-functions">Router Administration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>