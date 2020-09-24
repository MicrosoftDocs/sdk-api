---
UID: NF:mprapi.MprConfigInterfaceDelete
title: MprConfigInterfaceDelete function (mprapi.h)
description: The MprConfigInterfaceDelete function removes a router interface from the router configuration. All transport information associated with this interface is also removed.
helpviewer_keywords: ["MprConfigInterfaceDelete","MprConfigInterfaceDelete function [RAS]","_mpr_mprconfiginterfacedelete","mprapi/MprConfigInterfaceDelete","rras.mprconfiginterfacedelete"]
old-location: rras\mprconfiginterfacedelete.htm
tech.root: RRAS
ms.assetid: 1777f742-8037-40d9-8279-b4bb89ea6f0d
ms.date: 12/05/2018
ms.keywords: MprConfigInterfaceDelete, MprConfigInterfaceDelete function [RAS], _mpr_mprconfiginterfacedelete, mprapi/MprConfigInterfaceDelete, rras.mprconfiginterfacedelete
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
 - MprConfigInterfaceDelete
 - mprapi/MprConfigInterfaceDelete
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
 - MprConfigInterfaceDelete
---

# MprConfigInterfaceDelete function


## -description

The 
<b>MprConfigInterfaceDelete</b> function removes a router interface from the router configuration. All transport information associated with this interface is also removed.

## -parameters

### -param hMprConfig [in]

Handle to the router configuration. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>.

### -param hRouterInterface [in]

Handle to the interface configuration. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacecreate">MprConfigInterfaceCreate</a>, 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacegethandle">MprConfigInterfaceGetHandle</a>, or 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfaceenum">MprConfigInterfaceEnum</a>.

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
The <i>hMprConfig</i> parameter is <b>NULL</b>, or the <i>hRouterInterface</i> parameter is <b>NULL</b>, or both parameters are <b>NULL</b>.

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



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacecreate">MprConfigInterfaceCreate</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfaceenum">MprConfigInterfaceEnum</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacegethandle">MprConfigInterfaceGetHandle</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>



<a href="/windows/desktop/RRAS/router-configuration-functions">Router Configuration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>