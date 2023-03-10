---
UID: NF:ras.RasGetNapStatus
title: RasGetNapStatus function (ras.h)
description: Retrieves the Network Access Protection (NAP) connection state variables for a given remote access connection.
helpviewer_keywords: ["RasGetNapStatus","ras/rasgetnapstatus","rasgetnapstatus","rasgetnapstatus function [RAS]","rras.rasgetnapstatus"]
old-location: rras\rasgetnapstatus.htm
tech.root: RRAS
ms.assetid: 7f36f93f-7e07-4ad8-923f-59146bda4687
ms.date: 12/05/2018
ms.keywords: RasGetNapStatus, ras/rasgetnapstatus, rasgetnapstatus, rasgetnapstatus function [RAS], rras.rasgetnapstatus
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - RasGetNapStatus
 - ras/RasGetNapStatus
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
 - rasgetnapstatus
---

# RasGetNapStatus function


## -description

The <b>RasGetNapStatus</b> function retrieves the <a href="/windows/desktop/NAP/network-access-protection-start-page">Network Access Protection</a> (NAP) connection state variables for a given remote access connection.

## -parameters

### -param hRasconn [in]

A handle to the connection. Use <a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> or <a href="/windows/desktop/api/ras/nf-ras-rasenumconnectionsa">RasEnumConnections</a> to obtain this handle.

### -param pRasNapState [in, out]

A pointer to a <a href="/windows/desktop/api/ras/ns-ras-rasnapstate">RASNAPSTATE</a> structure. On input, the <b>dwSize</b> member of the structure must be set to <b>sizeof(RASNAPSTATE)</b>. On output, <i>pNapState</i> returns the NAP state of the RAS connection.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from <a href="/windows/desktop/RRAS/routing-and-remote-access-error-codes">Routing and Remote Access Error Codes</a> or Winerror.h.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_NAP_CAPABLE</b></dt>
</dl>
</td>
<td width="60%">
Connection corresponding to the <i>hRasConn</i> parameter is not configured for NAP.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwSize</i> parameter of the <a href="/windows/desktop/api/ras/ns-ras-rasnapstate">RASNAPSTATE</a> structure has an invalid size value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
Handle passed to the function is either <b>NULL</b> or invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_CONNECTION</b></dt>
</dl>
</td>
<td width="60%">
RASMAN could not find the handle in its list of handles.

</td>
</tr>
</table>