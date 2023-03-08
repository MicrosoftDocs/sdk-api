---
UID: NC:ras.RASDIALFUNC2
title: RASDIALFUNC2 (ras.h)
description: A RasDialFunc2 callback function is called by the RasDial function calls when a change of state occurs during a remote access connection process.
helpviewer_keywords: ["ERROR_AUTH_INTERNAL","ERROR_CANNOT_GET_LANA","ERROR_NETBIOS_ERROR","ERROR_SERVER_NOT_RESPONDING","RasDialFunc2","RasDialFunc2 callback","RasDialFunc2 callback function [RAS]","_ras_rasdialfunc2","ras/RasDialFunc2","rras.rasdialfunc2"]
old-location: rras\rasdialfunc2.htm
tech.root: RRAS
ms.assetid: a9395048-492b-42fb-b247-52999cee3f44
ms.date: 12/05/2018
ms.keywords: ERROR_AUTH_INTERNAL, ERROR_CANNOT_GET_LANA, ERROR_NETBIOS_ERROR, ERROR_SERVER_NOT_RESPONDING, RasDialFunc2, RasDialFunc2 callback, RasDialFunc2 callback function [RAS], _ras_rasdialfunc2, ras/RasDialFunc2, rras.rasdialfunc2
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RASDIALFUNC2
 - ras/RASDIALFUNC2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ras.h
api_name:
 - RasDialFunc2
---

# RASDIALFUNC2 callback function


## -description

A 
<b>RasDialFunc2</b> callback function is called by the 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> function calls when a change of state occurs during a remote access connection process. A 
<b>RasDialFunc2</b> function is similar to the 
<a href="/windows/desktop/api/ras/nc-ras-rasdialfunc1">RasDialFunc1</a> callback function, except that it provides additional information for multilink connections.

## -parameters

### -param unnamedParam1

### -param unnamedParam2

### -param unnamedParam3

### -param unnamedParam4

### -param unnamedParam5

### -param unnamedParam6

### -param unnamedParam7

#### - dwCallbackId [in]

Provides an application-defined value that was specified in the <b>dwCallbackId</b> member of the 
<a href="/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)">RASDIALPARAMS</a> structure passed to 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a>.


#### - dwError [in]

Specifies the error that has occurred. If no error has occurred, <i>dwError</i> is zero. 




The 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> function calls 
<b>RasDialFunc2</b> with <i>dwError</i> set to zero upon entry to each connection state. If an error occurs within a state, 
<b>RasDial</b> calls 
<b>RasDialFunc2</b> again with a nonzero <i>dwError</i> value.

In some error cases, the <i>dwExtendedError</i> parameter contains extended error information.


#### - dwExtendedError [in]

Specifies extended error information for certain nonzero values of <i>dwError</i>. For all other values of <i>dwError</i>, <i>dwExtendedError</i> is zero. 




The contents of <i>dwExtendedError</i> are defined for values of <i>dwError</i> as follows.

<table>
<tr>
<th>dwError</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ERROR_SERVER_NOT_RESPONDING"></a><a id="error_server_not_responding"></a><dl>
<dt><b>ERROR_SERVER_NOT_RESPONDING</b></dt>
</dl>
</td>
<td width="60%">
Specifies the NetBIOS error that occurred.

</td>
</tr>
<tr>
<td width="40%"><a id="ERROR_NETBIOS_ERROR"></a><a id="error_netbios_error"></a><dl>
<dt><b>ERROR_NETBIOS_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Specifies the NetBIOS error that occurred.

</td>
</tr>
<tr>
<td width="40%"><a id="ERROR_AUTH_INTERNAL"></a><a id="error_auth_internal"></a><dl>
<dt><b>ERROR_AUTH_INTERNAL</b></dt>
</dl>
</td>
<td width="60%">
Specifies an internal diagnostics code.

</td>
</tr>
<tr>
<td width="40%"><a id="ERROR_CANNOT_GET_LANA"></a><a id="error_cannot_get_lana"></a><dl>
<dt><b>ERROR_CANNOT_GET_LANA</b></dt>
</dl>
</td>
<td width="60%">
Specifies a routing error code, which is a RAS error.

</td>
</tr>
</table>
 


#### - dwSubEntry [in]

Specifies a subentry index for the phone-book entry associated with this connection. This value indicates the subentry that generated this call to the 
<b>RasDialFunc2</b> callback function.


#### - hrasconn [in]

Handle to the RAS connection, as returned by 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a>.


#### - rascs [in]

Specifies the 
<a href="/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)">RASCONNSTATE</a> enumerator value that indicates the state the 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> remote access connection process is about to enter.


#### - unMsg [in]

Specifies the type of event that has occurred. Currently, the only event defined is WM_RASDIALEVENT.

## -returns

If the 
<b>RasDialFunc2</b> function returns a nonzero value, 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> continues to send callback notifications.

If the 
<b>RasDialFunc2</b> function returns zero, 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> stops sending callback notifications for all subentries.

## -remarks

A 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> connection operation is suspended during a call to a 
<b>RasDialFunc2</b> callback function. For that reason, the 
<b>RasDialFunc2</b> implementation generally returns as quickly as possible. There are two exceptions to that rule. Asynchronous (slow) devices such as modems often have time-out periods measured in seconds rather than milliseconds; a slow return from a 
<b>RasDialFunc2</b> function is generally not a problem. The prompt return requirement also does not apply when <i>dwError</i> is nonzero, indicating that an error has occurred. It is safe, for example, to put up an error dialog box and wait for user input.

The 
<b>RasDialFunc2</b> implementation should not depend on the order or occurrence of particular 
<a href="/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)">RASCONNSTATE</a> connection states, because this may vary between platforms.

Do not call the 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> function from within a 
<b>RasDialFunc2</b> callback function. Call the 
<a href="/windows/desktop/api/ras/nf-ras-rasgetconnectstatusa">RasGetConnectStatus</a>, 
<a href="/windows/desktop/api/ras/nf-ras-rasenumentriesa">RasEnumEntries</a>, 
<a href="/windows/desktop/api/ras/nf-ras-rasenumconnectionsa">RasEnumConnections</a>, 
<a href="/windows/desktop/api/ras/nf-ras-rasgeterrorstringa">RasGetErrorString</a>, and 
<a href="/windows/desktop/api/ras/nf-ras-rashangupa">RasHangUp</a> functions from within the callback function. For example, calling 
<b>RasGetConnectStatus</b> from within a callback function would be useful for determining the name and type of the connecting device.

<div class="alert"><b>Note</b>  For convenience, 
<a href="/windows/desktop/api/ras/nf-ras-rashangupa">RasHangUp</a> can be called from within a 
<b>RasDialFunc2</b> callback function. However, much of the hang-up processing occurs after the 
<b>RasDialFunc2</b> callback function has returned.</div>
<div> </div>
<div class="alert"><b>Note</b>  <b>RasDialFunc2</b> is a placeholder for the application-defined or library-defined function name.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)">RASCONNSTATE</a>



<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a>



<a href="/windows/desktop/api/ras/nc-ras-rasdialfunc">RasDialFunc</a>



<a href="/windows/desktop/api/ras/nc-ras-rasdialfunc1">RasDialFunc1</a>



<a href="/windows/desktop/api/ras/nf-ras-rasenumconnectionsa">RasEnumConnections</a>



<a href="/windows/desktop/api/ras/nf-ras-rasenumentriesa">RasEnumEntries</a>



<a href="/windows/desktop/api/ras/nf-ras-rasgetconnectstatusa">RasGetConnectStatus</a>



<a href="/windows/desktop/api/ras/nf-ras-rasgeterrorstringa">RasGetErrorString</a>



<a href="/windows/desktop/api/ras/nf-ras-rashangupa">RasHangUp</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>