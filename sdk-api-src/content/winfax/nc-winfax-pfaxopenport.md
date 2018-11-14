---
UID: NC:winfax.PFAXOPENPORT
title: PFAXOPENPORT
author: windows-sdk-content
description: The FaxOpenPort function returns a fax port handle to a fax client application. The port handle is required when the application calls other fax client functions that facilitate device management and fax document routing.
old-location: fax\_mfax_faxopenport.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_15ro.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: FaxOpenPortA, FaxOpenPortW, PFAXOPENPORT, PFAXOPENPORT callback, PFAXOPENPORT callback function [Fax Service], PORT_OPEN_MODIFY, PORT_OPEN_QUERY, _mfax_faxopenport, fax._mfax_faxopenport, winfax/FaxOpenPortA, winfax/FaxOpenPortW, winfax/PFAXOPENPORT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxOpenPortW (Unicode) and FaxOpenPortA (ANSI)
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
 - Winfax.h
api_name:
 - PFAXOPENPORT
 - FaxOpenPortA
 - FaxOpenPortW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFAXOPENPORT callback function


## -description


The <b>FaxOpenPort</b> function returns a fax port handle to a fax client application. The port handle is required when the application calls other fax client functions that facilitate device management and fax document routing.


## -parameters




### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="https://msdn.microsoft.com/8705fb04-1047-4f83-ada9-898024ce719c">FaxConnectFaxServer</a> function.


### -param DeviceId [in]

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that is the permanent line identifier for the receiving device. Call the <a href="https://msdn.microsoft.com/7bd33e6f-09ff-449b-ac22-b79a14e5d928">FaxEnumPorts</a> function to retrieve a valid value for this parameter. For more information, see the following Remarks section.


### -param Flags [in]

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that contains a set of bit flags that defines the access level for the port. This parameter can be one or more of the following values.



#### PORT_OPEN_QUERY

Port access level required to obtain a fax port handle. This access level is also required to call the <a href="https://msdn.microsoft.com/1cf89b9c-525d-42df-b3fa-4dda6f560fd6">FaxGetPort</a> function to query fax port information.



#### PORT_OPEN_MODIFY

Port access level required to change the configuration of a fax port with a call to the <a href="https://msdn.microsoft.com/1cf89b9c-525d-42df-b3fa-4dda6f560fd6">FaxGetPort</a> function. This access level also includes the access rights associated with the <a href="https://msdn.microsoft.com/bd1d8a10-0867-4701-b6ef-d2f2f9f6923c">PORT_OPEN_QUERY</a> access level.


### -param FaxPortHandle [out]

Type: <b>LPHANDLE</b>

Pointer to a variable that receives a fax port handle that is required on subsequent calls to other fax client functions. If the fax server returns a <b>NULL</b> handle, it indicates an error.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. GetLastError can return one of the following errors.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access is denied. <a href="https://msdn.microsoft.com/7d6ff208-33e4-42b2-ae21-76ec8ff58809">FAX_PORT_QUERY</a> access is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
An error occurred during memory allocation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The port has already been opened with <a href="https://msdn.microsoft.com/bd1d8a10-0867-4701-b6ef-d2f2f9f6923c">PORT_OPEN_MODIFY</a> access.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_UNIT</b></dt>
</dl>
</td>
<td width="60%">
The <i>DeviceId</i> parameter is invalid.

</td>
</tr>
</table>
 




## -remarks



Call the <b>FaxOpenPort</b> function to obtain the handle to a fax port. Use the handle when you call the following functions:

<ul>
<li>
<a href="https://msdn.microsoft.com/32558e1f-c961-4fdc-806b-9544be4f95ee">FaxSetPort</a> to change the configuration of the port</li>
<li>
<a href="https://msdn.microsoft.com/1f78fed5-6b49-4946-8607-f1d7f9052aaa">FaxEnumRoutingMethods</a> to retrieve information about the fax routing methods associated with a device</li>
</ul>
The <a href="https://msdn.microsoft.com/7bd33e6f-09ff-449b-ac22-b79a14e5d928">FaxEnumPorts</a> function returns an array of <a href="https://msdn.microsoft.com/a1772290-7f78-49f2-a1e6-d312247995e4">FAX_PORT_INFO</a> structures. Each structure contains detailed information for one port, including a valid value to pass in the <i>DeviceId</i> parameter. An application should not save this device identifier in a persistent manner, because the identifier can change between function calls to the fax server.

For more information, see <a href="https://msdn.microsoft.com/fb00d78a-1aca-4be2-9b00-e322355c6b52">Fax Ports</a>, <a href="https://msdn.microsoft.com/784fdc0e-c664-4ea9-8a4f-0a0cd89c0d81">Fax Device Management</a>, and <a href="https://msdn.microsoft.com/356dda5c-852e-46b7-8fa4-f3a0c62d65cb">Managing Fax Routing Data</a>.




## -see-also




<a href="https://msdn.microsoft.com/a1772290-7f78-49f2-a1e6-d312247995e4">FAX_PORT_INFO</a>



<a href="https://msdn.microsoft.com/b076b5ba-09af-4312-90c1-27abd0b859df">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/8705fb04-1047-4f83-ada9-898024ce719c">FaxConnectFaxServer</a>



<a href="https://msdn.microsoft.com/7bd33e6f-09ff-449b-ac22-b79a14e5d928">FaxEnumPorts</a>



<a href="https://msdn.microsoft.com/1cf89b9c-525d-42df-b3fa-4dda6f560fd6">FaxGetPort</a>



<a href="https://msdn.microsoft.com/921007cf-a836-4e90-a544-b320eea2bd54">FaxInitializeEventQueue</a>



<a href="https://msdn.microsoft.com/32558e1f-c961-4fdc-806b-9544be4f95ee">FaxSetPort</a>
 

 

