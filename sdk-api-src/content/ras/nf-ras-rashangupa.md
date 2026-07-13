---
UID: NF:ras.RasHangUpA
title: RasHangUpA function (ras.h)
description: The RasHangUp function terminates a remote access connection. The connection is specified with a RAS connection handle. The function releases all RASAPI32.DLL resources associated with the handle. (ANSI)
helpviewer_keywords: ["RasHangUpA", "ras/RasHangUpA"]
old-location: rras\rashangup.htm
tech.root: RRAS
ms.assetid: b5720ddf-c7ac-439e-97cb-62240122a775
ms.date: 12/05/2018
ms.keywords: RasHangUp, RasHangUp function [RAS], RasHangUpA, RasHangUpW, _ras_rashangup, ras/RasHangUp, ras/RasHangUpA, ras/RasHangUpW, rras.rashangup
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasHangUpW (Unicode) and RasHangUpA (ANSI)
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
 - RasHangUpA
 - ras/RasHangUpA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rasapi32.dll
 - Ext-MS-Win-ras-rasapi32-l1-1-0.dll
 - Ext-MS-Win-ras-rasapi32-l1-1-1.dll
api_name:
 - RasHangUp
 - RasHangUpA
 - RasHangUpW
---

# RasHangUpA function


## -description

The 
<b>RasHangUp</b> function terminates a remote access connection. The connection is specified with a RAS connection handle. The function releases all RASAPI32.DLL resources associated with the handle.

## -parameters

### -param unnamedParam1 [in]

Specifies the remote access connection to terminate. This is a handle returned from a previous call to 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> or 
<a href="/windows/desktop/api/ras/nf-ras-rasenumconnectionsa">RasEnumConnections</a>.

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
The handle specified in <i>hrasconn</i> is invalid.

</td>
</tr>
</table>

## -remarks

The connection is terminated even if the 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> call has not yet been completed.

After this call, the <i>hrasconn</i> handle can no longer be used.

An application should not call 
<b>RasHangUp</b> and then immediately exit. The connection state machine needs time to properly terminate. If the system prematurely terminates the state machine, the state machine can fail to properly close a port, leaving the port in an inconsistent state. Also, an immediate attempt to use the same connection may fail leaving the connection unusable. A simple way to avoid these problems is to call 
<a href="/windows/desktop/api/synchapi/nf-synchapi-sleep">Sleep</a>(3000) after returning from 
<b>RasHangUp</b>; after that pause, the application can exit. A more responsive way to avoid these problems is, after returning from 
<b>RasHangUp</b>, to call 
<a href="/windows/desktop/api/ras/nf-ras-rasgetconnectstatusa">RasGetConnectStatus</a>(<i>hrasconn</i>) and <b>Sleep</b>(0) in a loop until 
<b>RasGetConnectStatus</b> returns <b>ERROR_INVALID_HANDLE</b>.

You can call 
<b>RasHangUp</b> on the handle returned by 
<a href="/windows/desktop/api/ras/nf-ras-rasgetsubentryhandlea">RasGetSubEntryHandle</a> to terminate a single link in a multi-link connection. However, in this case, you cannot use 
<a href="/windows/desktop/api/ras/nf-ras-rasgetconnectstatusa">RasGetConnectStatus</a> to determine if the link terminated; 
<b>RasGetConnectStatus</b> may not return <b>ERROR_INVALID_HANDLE</b> even though the link terminated successfully.





> [!NOTE]
> The ras.h header defines RasHangUp as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa376725(v=vs.85)">RASCONN</a>



<a href="/windows/desktop/api/ras/nc-ras-rascustomhangupfn">RasCustomHangUp</a>



<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a>



<a href="/windows/desktop/api/ras/nf-ras-rasenumconnectionsa">RasEnumConnections</a>



<a href="/windows/desktop/api/ras/nf-ras-rasgetconnectstatusa">RasGetConnectStatus</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-sleep">Sleep</a>
