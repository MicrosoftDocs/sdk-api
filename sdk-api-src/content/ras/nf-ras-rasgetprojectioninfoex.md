---
UID: NF:ras.RasGetProjectionInfoEx
title: RasGetProjectionInfoEx function (ras.h)
description: Obtains information about Point-to-Point Protocol (PPP) or Internet Key Exchange version 2 (IKEv2) remote access projection operations for all RAS connections on the local client.
helpviewer_keywords: ["RasGetProjectionInfoEx","RasGetProjectionInfoEx function [RAS]","ras/RasGetProjectionInfoEx","rras.rasgetprojectioninfoex"]
old-location: rras\rasgetprojectioninfoex.htm
tech.root: RRAS
ms.assetid: e34216ed-fa78-4cb3-8db9-274c8ba196dd
ms.date: 12/05/2018
ms.keywords: RasGetProjectionInfoEx, RasGetProjectionInfoEx function [RAS], ras/RasGetProjectionInfoEx, rras.rasgetprojectioninfoex
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RasGetProjectionInfoEx
 - ras/RasGetProjectionInfoEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rasapi32.dll
api_name:
 - RasGetProjectionInfoEx
---

# RasGetProjectionInfoEx function


## -description

The <b>RasGetProjectionInfoEx</b> function  obtains information about Point-to-Point Protocol (PPP) or Internet Key Exchange version 2 (IKEv2) remote access projection operations for all RAS connections on the local client.

## -parameters

### -param hrasconn [in]

A handle to the RAS connection for which the tunnel endpoints are to be changed. This can be a handle returned by the 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> or 
<a href="/windows/desktop/api/ras/nf-ras-rasenumconnectionsa">RasEnumConnections</a> function.

### -param pRasProjection [in, out]

A pointer to a <a href="/windows/desktop/api/ras/ns-ras-ras_projection_info">RAS_PROJECTION_INFO</a> structure that receives the projection information for the RAS connections.

### -param lpdwSize [in, out]

A pointer, in input, that specifies the size, in bytes, of the buffer pointed to by pRasProjection. On output, this variable receives the size, in bytes, of the buffer needed to store the number of <a href="/windows/desktop/api/ras/ns-ras-ras_projection_info">RAS_PROJECTION_INFO</a> structures pointed to by 
					<i>pRasProjection</i>.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from <a href="/windows/desktop/RRAS/routing-and-remote-access-error-codes">Routing and Remote Access Error Codes</a> or Winerror.h.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUFFER_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by <i>pRasProjection</i> is not large enough to contain the requested information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hrasconn</i> parameter is not a valid handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The function was called with an invalid parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwSize</i> member of the structure pointed to by <i>pRasProjection</i> specifies an invalid size.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PROTOCOL_NOT_CONFIGURED</b></dt>
</dl>
</td>
<td width="60%">
The control protocol for which information was requested neither succeeded nor failed, because the connection's phone-book entry did not require that an attempt to negotiate the protocol be made.

</td>
</tr>
</table>

## -remarks

Remote access projection is the process whereby a remote access server and a remote client negotiate network protocol-specific information. A remote access server uses this network protocol-specific information to represent a remote client on the network.

Remote access projection information is not available until the operating system has executed the <a href="/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)">RASCS_Projected</a> state on the remote access connection. If 
<b>RasGetProjectionInfoEx</b> is called prior to the <b>RASCS_Projected</b> state, it returns <b>ERROR_PROJECTION_NOT_COMPLETE</b>.

## -see-also

<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>