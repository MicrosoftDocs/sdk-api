---
UID: NF:ras.RasHangUpA
title: RasHangUpA function
author: windows-sdk-content
description: The RasHangUp function terminates a remote access connection. The connection is specified with a RAS connection handle. The function releases all RASAPI32.DLL resources associated with the handle.
old-location: rras\rashangup.htm
tech.root: RRAS
ms.assetid: b5720ddf-c7ac-439e-97cb-62240122a775
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: RasHangUp, RasHangUp function [RAS], RasHangUpA, RasHangUpW, _ras_rashangup, ras/RasHangUp, ras/RasHangUpA, ras/RasHangUpW, rras.rashangup
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RasHangUpA function


## -description


The 
<b>RasHangUp</b> function terminates a remote access connection. The connection is specified with a RAS connection handle. The function releases all RASAPI32.DLL resources associated with the handle.


## -parameters




### -param Arg1 [in]

Specifies the remote access connection to terminate. This is a handle returned from a previous call to 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> or 
<a href="https://msdn.microsoft.com/b581cfbf-a55e-4f56-89cd-168aa23af550">RasEnumConnections</a>.


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
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> call has not yet been completed.

After this call, the <i>hrasconn</i> handle can no longer be used.

An application should not call 
<b>RasHangUp</b> and then immediately exit. The connection state machine needs time to properly terminate. If the system prematurely terminates the state machine, the state machine can fail to properly close a port, leaving the port in an inconsistent state. Also, an immediate attempt to use the same connection may fail leaving the connection unusable. A simple way to avoid these problems is to call 
<a href="_win32_sleep">Sleep</a>(3000) after returning from 
<b>RasHangUp</b>; after that pause, the application can exit. A more responsive way to avoid these problems is, after returning from 
<b>RasHangUp</b>, to call 
<a href="https://msdn.microsoft.com/3b2a2f8d-b1ff-44d2-ba49-60877ca6c104">RasGetConnectStatus</a>(<i>hrasconn</i>) and <b>Sleep</b>(0) in a loop until 
<b>RasGetConnectStatus</b> returns <b>ERROR_INVALID_HANDLE</b>.

You can call 
<b>RasHangUp</b> on the handle returned by 
<a href="https://msdn.microsoft.com/020388b1-9965-4bd1-be7b-30f2127cb0fb">RasGetSubEntryHandle</a> to terminate a single link in a multi-link connection. However, in this case, you cannot use 
<a href="https://msdn.microsoft.com/3b2a2f8d-b1ff-44d2-ba49-60877ca6c104">RasGetConnectStatus</a> to determine if the link terminated; 
<b>RasGetConnectStatus</b> may not return <b>ERROR_INVALID_HANDLE</b> even though the link terminated successfully.




## -see-also




<a href="https://msdn.microsoft.com/234834e2-f539-42de-add7-63e93086de17">RASCONN</a>



<a href="https://msdn.microsoft.com/56410af3-7b23-4536-998d-88d78d45585d">RasCustomHangUp</a>



<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a>



<a href="https://msdn.microsoft.com/b581cfbf-a55e-4f56-89cd-168aa23af550">RasEnumConnections</a>



<a href="https://msdn.microsoft.com/3b2a2f8d-b1ff-44d2-ba49-60877ca6c104">RasGetConnectStatus</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>



<a href="_win32_sleep">Sleep</a>
 

 

