---
UID: NC:ras.RASDIALFUNC2
title: RASDIALFUNC2
author: windows-sdk-content
description: A RasDialFunc2 callback function is called by the RasDial function calls when a change of state occurs during a remote access connection process.
old-location: rras\rasdialfunc2.htm
tech.root: RRAS
ms.assetid: a9395048-492b-42fb-b247-52999cee3f44
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ERROR_AUTH_INTERNAL, ERROR_CANNOT_GET_LANA, ERROR_NETBIOS_ERROR, ERROR_SERVER_NOT_RESPONDING, RasDialFunc2, RasDialFunc2 callback, RasDialFunc2 callback function [RAS], _ras_rasdialfunc2, ras/RasDialFunc2, rras.rasdialfunc2
ms.topic: callback
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
 - RasDialFunc2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RASDIALFUNC2 callback function


## -description


A 
<b>RasDialFunc2</b> callback function is called by the 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> function calls when a change of state occurs during a remote access connection process. A 
<b>RasDialFunc2</b> function is similar to the 
<a href="https://msdn.microsoft.com/f0b0dbbc-8544-4711-819a-48bb714a67d9">RasDialFunc1</a> callback function, except that it provides additional information for multilink connections.


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3


### -param Arg4


### -param Arg5


### -param Arg6


### -param Arg7








#### - dwCallbackId [in]

Provides an application-defined value that was specified in the <b>dwCallbackId</b> member of the 
<a href="https://msdn.microsoft.com/13d15c98-a41b-4bc8-8be6-c0b718b86fea">RASDIALPARAMS</a> structure passed to 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a>.


#### - dwError [in]

Specifies the error that has occurred. If no error has occurred, <i>dwError</i> is zero. 




The 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> function calls 
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
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a>.


#### - rascs [in]

Specifies the 
<a href="https://msdn.microsoft.com/42047265-1b0f-4449-842c-e860b8fb6728">RASCONNSTATE</a> enumerator value that indicates the state the 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> remote access connection process is about to enter.


#### - unMsg [in]

Specifies the type of event that has occurred. Currently, the only event defined is WM_RASDIALEVENT.


## -returns



If the 
<b>RasDialFunc2</b> function returns a nonzero value, 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> continues to send callback notifications.

If the 
<b>RasDialFunc2</b> function returns zero, 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> stops sending callback notifications for all subentries.




## -remarks



A 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> connection operation is suspended during a call to a 
<b>RasDialFunc2</b> callback function. For that reason, the 
<b>RasDialFunc2</b> implementation generally returns as quickly as possible. There are two exceptions to that rule. Asynchronous (slow) devices such as modems often have time-out periods measured in seconds rather than milliseconds; a slow return from a 
<b>RasDialFunc2</b> function is generally not a problem. The prompt return requirement also does not apply when <i>dwError</i> is nonzero, indicating that an error has occurred. It is safe, for example, to put up an error dialog box and wait for user input.

The 
<b>RasDialFunc2</b> implementation should not depend on the order or occurrence of particular 
<a href="https://msdn.microsoft.com/42047265-1b0f-4449-842c-e860b8fb6728">RASCONNSTATE</a> connection states, because this may vary between platforms.

Do not call the 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> function from within a 
<b>RasDialFunc2</b> callback function. Call the 
<a href="https://msdn.microsoft.com/3b2a2f8d-b1ff-44d2-ba49-60877ca6c104">RasGetConnectStatus</a>, 
<a href="https://msdn.microsoft.com/9df7402f-c93e-45d4-925a-f2ce9d547bce">RasEnumEntries</a>, 
<a href="https://msdn.microsoft.com/b581cfbf-a55e-4f56-89cd-168aa23af550">RasEnumConnections</a>, 
<a href="https://msdn.microsoft.com/4d308dd8-e623-467b-836e-faace19460f1">RasGetErrorString</a>, and 
<a href="https://msdn.microsoft.com/b5720ddf-c7ac-439e-97cb-62240122a775">RasHangUp</a> functions from within the callback function. For example, calling 
<b>RasGetConnectStatus</b> from within a callback function would be useful for determining the name and type of the connecting device.

<div class="alert"><b>Note</b>  For convenience, 
<a href="https://msdn.microsoft.com/b5720ddf-c7ac-439e-97cb-62240122a775">RasHangUp</a> can be called from within a 
<b>RasDialFunc2</b> callback function. However, much of the hang-up processing occurs after the 
<b>RasDialFunc2</b> callback function has returned.</div>
<div> </div>
<div class="alert"><b>Note</b>  <b>RasDialFunc2</b> is a placeholder for the application-defined or library-defined function name.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/42047265-1b0f-4449-842c-e860b8fb6728">RASCONNSTATE</a>



<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a>



<a href="https://msdn.microsoft.com/668ebede-73ec-4ee9-9b81-7167e827db60">RasDialFunc</a>



<a href="https://msdn.microsoft.com/f0b0dbbc-8544-4711-819a-48bb714a67d9">RasDialFunc1</a>



<a href="https://msdn.microsoft.com/b581cfbf-a55e-4f56-89cd-168aa23af550">RasEnumConnections</a>



<a href="https://msdn.microsoft.com/9df7402f-c93e-45d4-925a-f2ce9d547bce">RasEnumEntries</a>



<a href="https://msdn.microsoft.com/3b2a2f8d-b1ff-44d2-ba49-60877ca6c104">RasGetConnectStatus</a>



<a href="https://msdn.microsoft.com/4d308dd8-e623-467b-836e-faace19460f1">RasGetErrorString</a>



<a href="https://msdn.microsoft.com/b5720ddf-c7ac-439e-97cb-62240122a775">RasHangUp</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

