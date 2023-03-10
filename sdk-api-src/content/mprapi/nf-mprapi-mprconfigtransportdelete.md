---
UID: NF:mprapi.MprConfigTransportDelete
title: MprConfigTransportDelete function (mprapi.h)
description: The MprConfigTransportDelete function removes the specified transport from the list of transports present in the specified router configuration.
helpviewer_keywords: ["MprConfigTransportDelete","MprConfigTransportDelete function [RAS]","_mpr_mprconfigtransportdelete","mprapi/MprConfigTransportDelete","rras.mprconfigtransportdelete"]
old-location: rras\mprconfigtransportdelete.htm
tech.root: RRAS
ms.assetid: e022d0bc-f5ae-4c04-80f7-40ec77e2fa80
ms.date: 12/05/2018
ms.keywords: MprConfigTransportDelete, MprConfigTransportDelete function [RAS], _mpr_mprconfigtransportdelete, mprapi/MprConfigTransportDelete, rras.mprconfigtransportdelete
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
 - MprConfigTransportDelete
 - mprapi/MprConfigTransportDelete
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
 - MprConfigTransportDelete
---

# MprConfigTransportDelete function


## -description

The 
<b>MprConfigTransportDelete</b> function removes the specified transport from the list of transports present in the specified router configuration.

## -parameters

### -param hMprConfig [in]

Handle to the router configuration from which to remove the transport. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>.

### -param hRouterTransport [in]

Handle to the configuration for the transport being deleted. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigtransportcreate">MprConfigTransportCreate</a> or 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigtransportgethandle">MprConfigTransportGetHandle</a>.

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
The <i>hMprConfig</i> parameter is <b>NULL</b>, or the <i>hRouterTransport</i> parameter is <b>NULL</b>, or both are <b>NULL</b>.

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



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigtransportcreate">MprConfigTransportCreate</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigtransportgethandle">MprConfigTransportGetHandle</a>



<a href="/windows/desktop/RRAS/router-configuration-functions">Router Configuration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>