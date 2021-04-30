---
UID: NF:ras.RasClearLinkStatistics
title: RasClearLinkStatistics function (ras.h)
description: The RasClearLinkStatistics functions clears any accumulated statistics for the specified link in a RAS multilink connection.
helpviewer_keywords: ["RasClearLinkStatistics","RasClearLinkStatistics function [RAS]","_ras_rasclearlinkstatistics","ras/RasClearLinkStatistics","rras.rasclearlinkstatistics"]
old-location: rras\rasclearlinkstatistics.htm
tech.root: RRAS
ms.assetid: cac356a9-092c-4db2-b0a4-aaacfc514e29
ms.date: 12/05/2018
ms.keywords: RasClearLinkStatistics, RasClearLinkStatistics function [RAS], _ras_rasclearlinkstatistics, ras/RasClearLinkStatistics, rras.rasclearlinkstatistics
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
 - RasClearLinkStatistics
 - ras/RasClearLinkStatistics
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
 - RasClearLinkStatistics
---

# RasClearLinkStatistics function


## -description

The 
<b>RasClearLinkStatistics</b> functions clears any accumulated statistics for the specified link in a RAS multilink connection.

## -parameters

### -param hRasConn [in]

Handle to the connection. Use 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> or 
<a href="/windows/desktop/api/ras/nf-ras-rasenumconnectionsa">RasEnumConnections</a> to obtain this handle.

### -param dwSubEntry [in]

Specifies the subentry that corresponds to the link for which to clear statistics.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwSubEntry</i> parameter is zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_CONNECTION</b></dt>
</dl>
</td>
<td width="60%">
RAS could not find a connected port that corresponds to the value in the <i>dwSubEntry</i> parameter.

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

<a href="/windows/desktop/api/ras/nf-ras-rasclearconnectionstatistics">RasClearConnectionStatistics</a>



<a href="/windows/desktop/api/ras/nf-ras-rasgetlinkstatistics">RasGetLinkStatistics</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>