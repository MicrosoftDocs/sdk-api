---
UID: NF:ras.RasGetConnectStatusA
title: RasGetConnectStatusA function (ras.h)
description: The RasGetConnectStatus function retrieves information on the current status of the specified remote access connection. An application can use this call to determine when an asynchronous RasDial call is complete. (ANSI)
helpviewer_keywords: ["RasGetConnectStatusA", "ras/RasGetConnectStatusA"]
old-location: rras\rasgetconnectstatus.htm
tech.root: RRAS
ms.assetid: 3b2a2f8d-b1ff-44d2-ba49-60877ca6c104
ms.date: 12/05/2018
ms.keywords: RasGetConnectStatus, RasGetConnectStatus function [RAS], RasGetConnectStatusA, RasGetConnectStatusW, _ras_rasgetconnectstatus, ras/RasGetConnectStatus, ras/RasGetConnectStatusA, ras/RasGetConnectStatusW, rras.rasgetconnectstatus
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasGetConnectStatusW (Unicode) and RasGetConnectStatusA (ANSI)
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
 - RasGetConnectStatusA
 - ras/RasGetConnectStatusA
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
 - RasGetConnectStatus
 - RasGetConnectStatusA
 - RasGetConnectStatusW
---

# RasGetConnectStatusA function


## -description

The 
<b>RasGetConnectStatus</b> function retrieves information on the current status of the specified remote access connection. An application can use this call to determine when an asynchronous 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> call is complete.

## -parameters

### -param unnamedParam1 [in]

Specifies the remote access connection for which to retrieve the status. This handle must have been obtained from 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> or 
<a href="/windows/desktop/api/ras/nf-ras-rasenumconnectionsa">RasEnumConnections</a>.

### -param unnamedParam2 [in, out]

Pointer to the 
<a href="/previous-versions/windows/desktop/legacy/aa376728(v=vs.85)">RASCONNSTATUS</a> structure that, on output, receives the status information. 




On input, set the <b>dwSize</b> member of the structure to sizeof(<a href="/previous-versions/windows/desktop/legacy/aa376728(v=vs.85)">RASCONNSTATUS</a>) in order to identify the version of the structure being passed.

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
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The function could not allocate sufficient memory to complete the operation.

</td>
</tr>
</table>

## -remarks

The return value for 
<b>RasGetConnectStatus</b> is not necessarily equal to the value of the <b>dwError</b> member of the 
<a href="/previous-versions/windows/desktop/legacy/aa376728(v=vs.85)">RASCONNSTATUS</a> structure returned by 
<b>RasGetConnectStatus</b>. The return value of 
<b>RasGetConnectStatus</b> indicates errors that occur during the 
<b>RasGetConnectStatus</b> function call, whereas the <b>dwError</b> member indicates errors that prevented the connection from being established.





> [!NOTE]
> The ras.h header defines RasGetConnectStatus as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa376728(v=vs.85)">RASCONNSTATUS</a>



<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a>



<a href="/windows/desktop/api/ras/nf-ras-rasenumconnectionsa">RasEnumConnections</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>
