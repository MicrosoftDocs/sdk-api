---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# TcOpenInterfaceW function


## -description


The 
<b>TcOpenInterface</b> function opens an interface. The 
<b>TcOpenInterface</b> function identifies and opens an interface based on its text string, which is available from a call to 
<a href="https://msdn.microsoft.com/e6fbaa17-6b4b-45a2-baf7-898864a797b7">TcEnumerateInterfaces</a>. Once an interface is opened, the client must be prepared to receive notification regarding the open interface, through traffic control's use of the interface context.


## -parameters




### -param pInterfaceName [in]

Pointer to the text string identifying the interface to be opened. This text string is part of the information returned in a previous call to 
<a href="https://msdn.microsoft.com/e6fbaa17-6b4b-45a2-baf7-898864a797b7">TcEnumerateInterfaces</a>.


### -param ClientHandle [in]

Handle used by traffic control to identify the client, obtained through the <i>pClientHandle</i> parameter of the client's call to 
<a href="https://msdn.microsoft.com/10bbc08d-4bfa-4a64-b5b8-b720d7bc3185">TcRegisterClient</a>.


### -param ClIfcCtx [in]

Client's interface–context handle for the opened interface. Used as a callback parameter by traffic control when communicating with the client about the opened interface. This can be a container to hold an arbitrary client-defined context for this instance of the interface.


### -param pIfcHandle [out]

Pointer to the buffer where traffic control can return an interface handle. The interface handle returned to <i>pIfcHandle</i> must be used by the client to identify the interface in subsequent calls to traffic control.


## -returns



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NO_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The function executed without errors.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system is out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Traffic control failed to find an interface with the name provided in <i>pInterfaceName</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The client handle is invalid.

</td>
</tr>
</table>
 




## -remarks



Use of the 
<b>TcOpenInterface</b> function requires administrative privilege.




## -see-also




<a href="https://msdn.microsoft.com/cacf4c21-d831-462c-b9e8-fd51fcf8e4e4">ClNotifyHandler</a>



<a href="https://msdn.microsoft.com/e6fbaa17-6b4b-45a2-baf7-898864a797b7">TcEnumerateInterfaces</a>



<a href="https://msdn.microsoft.com/10bbc08d-4bfa-4a64-b5b8-b720d7bc3185">TcRegisterClient</a>
 

 

