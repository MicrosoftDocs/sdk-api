---
UID: NC:ras.RASDIALFUNC1
title: RASDIALFUNC1 (ras.h)
description: A RasDialFunc1 function is called by the RasDial function when a change of state occurs during a remote access connection process.helpviewer_keywords: ["ERROR_AUTH_INTERNAL","ERROR_CANNOT_GET_LANA","ERROR_NETBIOS_ERROR","ERROR_SERVER_NOT_RESPONDING","RasDialFunc1","RasDialFunc1 callback","RasDialFunc1 callback function [RAS]","_ras_rasdialfunc1","ras/RasDialFunc1","rras.rasdialfunc1"]
old-location: rras\rasdialfunc1.htm
tech.root: RRAS
ms.assetid: f0b0dbbc-8544-4711-819a-48bb714a67d9
ms.date: 12/05/2018
ms.keywords: ERROR_AUTH_INTERNAL, ERROR_CANNOT_GET_LANA, ERROR_NETBIOS_ERROR, ERROR_SERVER_NOT_RESPONDING, RasDialFunc1, RasDialFunc1 callback, RasDialFunc1 callback function [RAS], _ras_rasdialfunc1, ras/RasDialFunc1, rras.rasdialfunc1
f1_keywords:
- ras/RasDialFunc1
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- Ras.h
api_name:
- RasDialFunc1
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RASDIALFUNC1 callback function


## -description


A 
<b>RasDialFunc1</b> function is called by the 
<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> function  when a change of state occurs during a remote access connection process. A 
<b>RasDialFunc1</b> function is comparable to a 
<a href="https://docs.microsoft.com/windows/desktop/api/ras/nc-ras-rasdialfunc">RasDialFunc</a> function, but is enhanced by the addition of two parameters: a handle to the RAS connection, and an extended error code.


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3


### -param Arg4


### -param Arg5








#### - dwError [in]

Specifies the error that has occurred. If no error has occurred, <i>dwError</i> is zero. 





<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> calls 
<b>RasDialFunc1</b> with <i>dwError</i> set to zero upon entry to each connection state. If an error occurs within a state, 
<b>RasDial</b> calls 
<b>RasDialFunc1</b> again with a nonzero <i>dwError</i> value.

In some error cases, the <i>dwExtendedError</i> parameter contains extended error information.


#### - dwExtendedError [in]

Specifies extended error information for certain nonzero values of <i>dwError</i>. For all other values of <i>dwError, dwExtendedError</i> is zero. 




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
 


#### - hrasconn [in]

Handle to the RAS connection, as returned by 
<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a>.


#### - rascs [in]

Specifies the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)">RASCONNSTATE</a> enumerator value that indicates the state the 
<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> remote access connection process is about to enter.


#### - unMsg [in]

Specifies the type of event that has occurred. Currently, the only event defined is WM_RASDIALEVENT.


## -remarks



A 
<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> connection operation is suspended during a call to a 
<b>RasDialFunc1</b> callback function. For that reason, the 
<b>RasDialFunc1</b> implementation generally returns as quickly as possible. There are two exceptions to that rule. Asynchronous (slow) devices such as modems often have time-out periods measured in seconds rather than milliseconds; a slow return from a 
<b>RasDialFunc1</b> function is generally not a problem. The prompt return requirement also does not apply when <i>dwError</i> is nonzero, indicating that an error has occurred. It is safe, for example, to put up an error dialog box and wait for user input.

The 
<b>RasDialFunc1</b> implementation should not depend on the order or occurrence of particular 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)">RASCONNSTATE</a> connection states, because this may vary between platforms.

Do not call the 
<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> function from within a 
<b>RasDialFunc1</b> callback function. Call the 
<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasgetconnectstatusa">RasGetConnectStatus</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasenumentriesa">RasEnumEntries</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasenumconnectionsa">RasEnumConnections</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasgeterrorstringa">RasGetErrorString</a>, and 
<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rashangupa">RasHangUp</a> functions from within the callback function. For example, calling 
<b>RasGetConnectStatus</b> from within a callback function would be useful for determining the name and type of the connecting device.

Note that, for convenience, 
<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rashangupa">RasHangUp</a> can be called from within a 
<b>RasDialFunc1</b> callback function. However, much of the hang-up processing occurs after the 
<b>RasDialFunc1</b> callback function has returned.

<b>RasDialFunc1</b> is a placeholder for the application-defined or library-defined function name.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)">RASCONNSTATE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ras/nc-ras-rasdialfunc">RasDialFunc</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ras/nc-ras-rasdialfunc2">RasDialFunc2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasenumconnectionsa">RasEnumConnections</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasenumentriesa">RasEnumEntries</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasgetconnectstatusa">RasGetConnectStatus</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasgeterrorstringa">RasGetErrorString</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rashangupa">RasHangUp</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>
 

 

