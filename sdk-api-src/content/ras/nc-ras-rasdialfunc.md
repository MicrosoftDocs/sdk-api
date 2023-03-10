---
UID: NC:ras.RASDIALFUNC
title: RASDIALFUNC (ras.h)
description: The RasDialFunc callback function is called by the RasDial function when a change of state occurs during a RAS connection process.
helpviewer_keywords: ["RasDialFunc","RasDialFunc callback","RasDialFunc callback function [RAS]","_ras_rasdialfunc","ras/RasDialFunc","rras.rasdialfunc"]
old-location: rras\rasdialfunc.htm
tech.root: RRAS
ms.assetid: 668ebede-73ec-4ee9-9b81-7167e827db60
ms.date: 12/05/2018
ms.keywords: RasDialFunc, RasDialFunc callback, RasDialFunc callback function [RAS], _ras_rasdialfunc, ras/RasDialFunc, rras.rasdialfunc
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
 - RASDIALFUNC
 - ras/RASDIALFUNC
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
 - RasDialFunc
---

# RASDIALFUNC callback function


## -description

The 
<b>RasDialFunc</b> callback function is called by the 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> function  when a change of state occurs during a RAS connection process.

## -parameters

### -param unnamedParam1

### -param unnamedParam2

### -param unnamedParam3

#### - dwError [in]

Specifies the error that has occurred, or zero if no error has occurred. 





<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> calls 
<b>RasDialFunc</b> with <i>dwError</i> set to zero upon entry to each connection state. If an error occurs within a state, 
<b>RasDialFunc</b> is called again with a nonzero <i>dwError</i> value.


#### - rasconnstate [in]

Specifies the 
<a href="/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)">RASCONNSTATE</a> enumerator value that indicates the state the 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> remote access connection process is about to enter.


#### - unMsg [in]

Specifies the type of event that has occurred. Currently, the only event defined is WM_RASDIALEVENT.

## -remarks

A 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> connection operation is suspended during a call to a 
<b>RasDialFunc</b> callback function. For that reason, the 
<b>RasDialFunc</b> implementation should generally return as quickly as possible. There are two exceptions to that rule. Asynchronous (slow) devices such as modems often have time-out periods measured in seconds rather than milliseconds; a slow return from a 
<b>RasDialFunc</b> function is generally not a problem. The prompt return requirement also does not apply when <i>dwError</i> is nonzero, indicating that an error has occurred. It is safe, for example, to put up an error dialog box and wait for user input.

The 
<b>RasDialFunc</b> implementation should not depend on the order or occurrence of particular 
<a href="/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)">RASCONNSTATE</a> connection states, because this may vary between platforms.

Do not call the 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> function from within a 
<b>RasDialFunc</b> callback function. Call the 
<a href="/windows/desktop/api/ras/nf-ras-rasgetconnectstatusa">RasGetConnectStatus</a>, 
<a href="/windows/desktop/api/ras/nf-ras-rasenumentriesa">RasEnumEntries</a>, 
<a href="/windows/desktop/api/ras/nf-ras-rasenumconnectionsa">RasEnumConnections</a>, 
<a href="/windows/desktop/api/ras/nf-ras-rasgeterrorstringa">RasGetErrorString</a>, and 
<a href="/windows/desktop/api/ras/nf-ras-rashangupa">RasHangUp</a> functions from within the callback function. For example, calling 
<b>RasGetConnectStatus</b> from within a callback function would be useful to  determine the name and type of the connecting device.

<div class="alert"><b>Note</b>  For convenience, 
<a href="/windows/desktop/api/ras/nf-ras-rashangupa">RasHangUp</a> can be called from within a 
<b>RasDialFunc</b> callback function. However, much of the hang-up processing occurs after the 
<b>RasDialFunc</b> callback function has returned.</div>
<div> </div>
<div class="alert"><b>Note</b>  <b>RasDialFunc</b> is a placeholder for the application-defined or library-defined function name.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)">RASCONNSTATE</a>



<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a>



<a href="/windows/desktop/api/ras/nc-ras-rasdialfunc1">RasDialFunc1</a>



<a href="/windows/desktop/api/ras/nc-ras-rasdialfunc2">RasDialFunc2</a>



<a href="/windows/desktop/api/ras/nf-ras-rasenumconnectionsa">RasEnumConnections</a>



<a href="/windows/desktop/api/ras/nf-ras-rasenumentriesa">RasEnumEntries</a>



<a href="/windows/desktop/api/ras/nf-ras-rasgetconnectstatusa">RasGetConnectStatus</a>



<a href="/windows/desktop/api/ras/nf-ras-rasgeterrorstringa">RasGetErrorString</a>



<a href="/windows/desktop/api/ras/nf-ras-rashangupa">RasHangUp</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>