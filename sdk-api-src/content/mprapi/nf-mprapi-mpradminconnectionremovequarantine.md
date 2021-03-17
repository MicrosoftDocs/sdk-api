---
UID: NF:mprapi.MprAdminConnectionRemoveQuarantine
title: MprAdminConnectionRemoveQuarantine function (mprapi.h)
description: The MprAdminConnectionRemoveQuarantine function removes quarantine filters on a dialed-in RAS client if the filters were applied as a result of Internet Authentication Service (IAS) policies.
helpviewer_keywords: ["MprAdminConnectionRemoveQuarantine","MprAdminConnectionRemoveQuarantine function [RAS]","_mpr_mpradminconnectionremovequarantine","mprapi/MprAdminConnectionRemoveQuarantine","rras.mpradminconnectionremovequarantine"]
old-location: rras\mpradminconnectionremovequarantine.htm
tech.root: RRAS
ms.assetid: 9d8c33b4-4227-4538-bc0e-f663d1d560f1
ms.date: 12/05/2018
ms.keywords: MprAdminConnectionRemoveQuarantine, MprAdminConnectionRemoveQuarantine function [RAS], _mpr_mpradminconnectionremovequarantine, mprapi/MprAdminConnectionRemoveQuarantine, rras.mpradminconnectionremovequarantine
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - MprAdminConnectionRemoveQuarantine
 - mprapi/MprAdminConnectionRemoveQuarantine
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
 - MprAdminConnectionRemoveQuarantine
---

# MprAdminConnectionRemoveQuarantine function


## -description

The 
<b>MprAdminConnectionRemoveQuarantine</b> function removes quarantine filters on a dialed-in RAS client if the filters were applied as a result of Internet Authentication Service (IAS) policies.

## -parameters

### -param hRasServer [in]

Handle to the RAS server that services the connection. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>.

### -param hRasConnection [in]

Handle to connection for the RAS client for which to remove the quarantine filters. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionenum">MprAdminConnectionEnum</a>. 




Alternatively, this parameter specifies the IP address of the RAS client for which to remove the quarantine filter. The IP address should be specified as a <b>DWORD</b> in network byte order. Obtain the IP address by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionenum">MprAdminConnectionEnum</a>. If this parameter specifies an IP address, the <i>fIsIpAddress</i> parameter should specify a <b>TRUE</b> value.

### -param fIsIpAddress [in]

Specifies a Boolean value that indicates whether the <i>hRasConnection</i> parameter specifies the IP address of the client for which to remove the quarantine filters. If this parameter is a <b>TRUE</b> value, <i>hRasConnection</i> specifies an IP address. Otherwise, <i>hRasConnection</i> specifies a handle to a connection.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

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
The handle to the RAS server or the handle to the RAS connection is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The RAS client is not in quarantine.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
An error from MprError.h, RasError.h, or WinError.h.

</td>
</tr>
</table>

## -remarks

If <a href="/previous-versions/ms688288(v=vs.85)">Internet Authentication Service (IAS)</a> policies configure regular filters, then these filters are added to the RAS client interface as a result of calling 
<b>MprAdminConnectionRemoveQuarantine</b>.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionenum">MprAdminConnectionEnum</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>



<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>