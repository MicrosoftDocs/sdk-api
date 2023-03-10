---
UID: NF:ras.RasClearConnectionStatistics
title: RasClearConnectionStatistics function (ras.h)
description: The RasClearConnectionStatistics functions clears any accumulated statistics for the specified RAS connection.
helpviewer_keywords: ["RasClearConnectionStatistics","RasClearConnectionStatistics function [RAS]","_ras_rasclearconnectionstatistics","ras/RasClearConnectionStatistics","rras.rasclearconnectionstatistics"]
old-location: rras\rasclearconnectionstatistics.htm
tech.root: RRAS
ms.assetid: b5c87ecd-4f21-46b5-91a3-41706907157a
ms.date: 12/05/2018
ms.keywords: RasClearConnectionStatistics, RasClearConnectionStatistics function [RAS], _ras_rasclearconnectionstatistics, ras/RasClearConnectionStatistics, rras.rasclearconnectionstatistics
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RasClearConnectionStatistics
 - ras/RasClearConnectionStatistics
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
 - RasClearConnectionStatistics
---

# RasClearConnectionStatistics function


## -description

The 
<b>RasClearConnectionStatistics</b> functions clears any accumulated statistics for the specified RAS connection.

## -parameters

### -param hRasConn [in]

Handle to the connection. Use 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> or 
<a href="/windows/desktop/api/ras/nf-ras-rasenumconnectionsa">RasEnumConnections</a> to obtain this handle.

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
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hRasConn</i> parameter does not specify a valid connection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The function could not allocate sufficient memory to complete the operation.

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

## -see-also

<a href="/windows/desktop/api/ras/ns-ras-ras_stats">RAS_STATS</a>



<a href="/windows/desktop/api/ras/nf-ras-rasclearlinkstatistics">RasClearLinkStatistics</a>



<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a>



<a href="/windows/desktop/api/ras/nf-ras-rasenumconnectionsa">RasEnumConnections</a>



<a href="/windows/desktop/api/ras/nf-ras-rasgetconnectionstatistics">RasGetConnectionStatistics</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>