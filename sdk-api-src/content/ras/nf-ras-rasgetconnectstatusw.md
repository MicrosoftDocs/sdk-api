---
UID: NF:ras.RasGetConnectStatusW
title: RasGetConnectStatusW function (ras.h)
description: The RasGetConnectStatus function retrieves information on the current status of the specified remote access connection. An application can use this call to determine when an asynchronous RasDial call is complete.
old-location: rras\rasgetconnectstatus.htm
tech.root: RRAS
ms.assetid: 3b2a2f8d-b1ff-44d2-ba49-60877ca6c104
ms.date: 12/05/2018
ms.keywords: RasGetConnectStatus, RasGetConnectStatus function [RAS], RasGetConnectStatusA, RasGetConnectStatusW, _ras_rasgetconnectstatus, ras/RasGetConnectStatus, ras/RasGetConnectStatusA, ras/RasGetConnectStatusW, rras.rasgetconnectstatus
f1_keywords:
- ras/RasGetConnectStatus
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
req.unicode-ansi: RasGetConnectStatusW (Unicode) and RasGetConnectStatusA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RasGetConnectStatusW function


## -description


The 
<b>RasGetConnectStatus</b> function retrieves information on the current status of the specified remote access connection. An application can use this call to determine when an asynchronous 
<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> call is complete.


## -parameters




### -param arg1 [in]

Specifies the remote access connection for which to retrieve the status. This handle must have been obtained from 
<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> or 
<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasenumconnectionsa">RasEnumConnections</a>.


### -param arg2 [in, out]

Pointer to the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa376728(v=vs.85)">RASCONNSTATUS</a> structure that, on output, receives the status information. 




On input, set the <b>dwSize</b> member of the structure to sizeof(<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa376728(v=vs.85)">RASCONNSTATUS</a>) in order to identify the version of the structure being passed.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from <a href="https://docs.microsoft.com/windows/desktop/RRAS/routing-and-remote-access-error-codes">Routing and Remote Access Error Codes</a> or Winerror.h.

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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa376728(v=vs.85)">RASCONNSTATUS</a> structure returned by 
<b>RasGetConnectStatus</b>. The return value of 
<b>RasGetConnectStatus</b> indicates errors that occur during the 
<b>RasGetConnectStatus</b> function call, whereas the <b>dwError</b> member indicates errors that prevented the connection from being established.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa376728(v=vs.85)">RASCONNSTATUS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasenumconnectionsa">RasEnumConnections</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>
 

 

