---
UID: NF:ras.RasGetConnectStatusA
title: RasGetConnectStatusA function (ras.h)
author: windows-sdk-content
description: The RasGetConnectStatus function retrieves information on the current status of the specified remote access connection. An application can use this call to determine when an asynchronous RasDial call is complete.
old-location: rras\rasgetconnectstatus.htm
tech.root: RRAS
ms.assetid: 3b2a2f8d-b1ff-44d2-ba49-60877ca6c104
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RasGetConnectStatus, RasGetConnectStatus function [RAS], RasGetConnectStatusA, RasGetConnectStatusW, _ras_rasgetconnectstatus, ras/RasGetConnectStatus, ras/RasGetConnectStatusA, ras/RasGetConnectStatusW, rras.rasgetconnectstatus
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RasGetConnectStatusA function


## -description


The 
<b>RasGetConnectStatus</b> function retrieves information on the current status of the specified remote access connection. An application can use this call to determine when an asynchronous 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> call is complete.


## -parameters




### -param arg1 [in]

Specifies the remote access connection for which to retrieve the status. This handle must have been obtained from 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> or 
<a href="https://msdn.microsoft.com/b581cfbf-a55e-4f56-89cd-168aa23af550">RasEnumConnections</a>.


### -param arg2 [in, out]

Pointer to the 
<a href="https://msdn.microsoft.com/bebfab0c-96b2-4f34-917c-8f4cdf05bc2b">RASCONNSTATUS</a> structure that, on output, receives the status information. 




On input, set the <b>dwSize</b> member of the structure to sizeof(<a href="https://msdn.microsoft.com/bebfab0c-96b2-4f34-917c-8f4cdf05bc2b">RASCONNSTATUS</a>) in order to identify the version of the structure being passed.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from <a href="https://msdn.microsoft.com/1fa41438-7c93-4e9c-851c-652fba23da4f">Routing and Remote Access Error Codes</a> or Winerror.h.

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
<a href="https://msdn.microsoft.com/bebfab0c-96b2-4f34-917c-8f4cdf05bc2b">RASCONNSTATUS</a> structure returned by 
<b>RasGetConnectStatus</b>. The return value of 
<b>RasGetConnectStatus</b> indicates errors that occur during the 
<b>RasGetConnectStatus</b> function call, whereas the <b>dwError</b> member indicates errors that prevented the connection from being established.




## -see-also




<a href="https://msdn.microsoft.com/bebfab0c-96b2-4f34-917c-8f4cdf05bc2b">RASCONNSTATUS</a>



<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a>



<a href="https://msdn.microsoft.com/b581cfbf-a55e-4f56-89cd-168aa23af550">RasEnumConnections</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

