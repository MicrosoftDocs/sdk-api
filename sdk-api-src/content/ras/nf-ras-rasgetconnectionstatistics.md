---
UID: NF:ras.RasGetConnectionStatistics
title: RasGetConnectionStatistics function (ras.h)
description: The RasGetConnectionStatistics function retrieves accumulated connection statistics for the specified connection.
helpviewer_keywords: ["RasGetConnectionStatistics","RasGetConnectionStatistics function [RAS]","_ras_rasgetconnectionstatistics","ras/RasGetConnectionStatistics","rras.rasgetconnectionstatistics"]
old-location: rras\rasgetconnectionstatistics.htm
tech.root: RRAS
ms.assetid: 2db03535-c2bd-4e04-a86f-e68fe5c1f805
ms.date: 12/05/2018
ms.keywords: RasGetConnectionStatistics, RasGetConnectionStatistics function [RAS], _ras_rasgetconnectionstatistics, ras/RasGetConnectionStatistics, rras.rasgetconnectionstatistics
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
 - RasGetConnectionStatistics
 - ras/RasGetConnectionStatistics
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ras-rasapi32-l1-1-2.dll
 - Rasapi32.dll
 - Ext-MS-Win-ras-rasapi32-l1-1-0.dll
 - Ext-MS-Win-ras-rasapi32-l1-1-1.dll
api_name:
 - RasGetConnectionStatistics
---

# RasGetConnectionStatistics function


## -description

The 
<b>RasGetConnectionStatistics</b> function retrieves accumulated connection statistics for the specified connection.

## -parameters

### -param hRasConn [in]

Handle to the connection. Use <a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> or <a href="/windows/desktop/api/ras/nf-ras-rasenumconnectionsa">RasEnumConnections</a> to obtain this handle.

### -param lpStatistics [in, out]

Pointer to the 
<a href="/windows/desktop/api/ras/ns-ras-ras_stats">RAS_STATS</a> structure that, on output, receives the statistics. 




On input, set the <b>dwSize</b> member of this structure to sizeof(<a href="/windows/desktop/api/ras/ns-ras-ras_stats">RAS_STATS</a>).

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
At least one of the following is true: the <i>hRasConn</i> parameter is zero, the <i>lpStatistics</i> parameter is <b>NULL</b>, or the value specified by the <b>dwSize</b> member of the 
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

<a href="/windows/desktop/api/ras/nf-ras-rasclearconnectionstatistics">RasClearConnectionStatistics</a>



<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a>



<a href="/windows/desktop/api/ras/nf-ras-rasenumconnectionsa">RasEnumConnections</a>



<a href="/windows/desktop/api/ras/nf-ras-rasgetlinkstatistics">RasGetLinkStatistics</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>