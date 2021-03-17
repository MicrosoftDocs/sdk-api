---
UID: NF:ras.RasGetLinkStatistics
title: RasGetLinkStatistics function (ras.h)
description: The RasGetLinkStatistics function retrieves accumulated statistics for the specified link in a RAS multilink connection.
helpviewer_keywords: ["RasGetLinkStatistics","RasGetLinkStatistics function [RAS]","_ras_rasgetlinkstatistics","ras/RasGetLinkStatistics","rras.rasgetlinkstatistics"]
old-location: rras\rasgetlinkstatistics.htm
tech.root: RRAS
ms.assetid: 825a80c9-8023-4b7f-a303-f1eaa650e1d8
ms.date: 12/05/2018
ms.keywords: RasGetLinkStatistics, RasGetLinkStatistics function [RAS], _ras_rasgetlinkstatistics, ras/RasGetLinkStatistics, rras.rasgetlinkstatistics
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
 - RasGetLinkStatistics
 - ras/RasGetLinkStatistics
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
 - RasGetLinkStatistics
---

# RasGetLinkStatistics function


## -description

The 
<b>RasGetLinkStatistics</b> function retrieves accumulated statistics for the specified link in a RAS multilink connection.

## -parameters

### -param hRasConn [in]

Handle to the connection. Use 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> or 
<a href="/windows/desktop/api/ras/nf-ras-rasenumconnectionsa">RasEnumConnections</a> to obtain this handle.

### -param dwSubEntry [in]

Specifies the subentry that corresponds to the link for which to retrieve statistics.

### -param lpStatistics [in, out]

Pointer to the 
<a href="/windows/desktop/api/ras/ns-ras-ras_stats">RAS_STATS</a> structure that, on output, receives the statistics. 




On input, the <b>dwSize</b> member of this structure specifies the size of 
<a href="/windows/desktop/api/ras/ns-ras-ras_stats">RAS_STATS</a>. Use sizeof(<b>RAS_STATS</b>) to obtain this size.

This parameter cannot be <b>NULL</b>.

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
<dt><b>E_INVALID_ARG</b></dt>
</dl>
</td>
<td width="60%">
At least one of the following is true: the <i>hRasConn</i> parameter is zero, the <i>dwSubEntry</i> parameter is zero, the <i>lpStatistics</i> parameter is <b>NULL</b>, or the value specified by the <b>dwSize</b> member of the 
<a href="/windows/desktop/api/ras/ns-ras-ras_stats">RAS_STATS</a> structure specifies a version of the structure that is not supported by the operating system in use.

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

<a href="/windows/desktop/api/ras/nf-ras-rasclearlinkstatistics">RasClearLinkStatistics</a>



<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a>



<a href="/windows/desktop/api/ras/nf-ras-rasenumconnectionsa">RasEnumConnections</a>



<a href="/windows/desktop/api/ras/nf-ras-rasgetconnectionstatistics">RasGetConnectionStatistics</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>