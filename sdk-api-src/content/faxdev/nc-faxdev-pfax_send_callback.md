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

# PFAX_SEND_CALLBACK callback function


## -description


The <i>FaxSendCallback</i> function is an application-defined or library-defined callback function that a fax service provider (FSP) calls to notify the fax service that an outgoing fax call is in progress.

The <b>PFAX_SEND_CALLBACK</b> data type is a pointer to a <i>FaxSendCallback</i> function. <i>FaxSendCallback</i> is a placeholder for an application-defined or library-defined function name.


## -parameters




### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax handle returned by the <a href="https://msdn.microsoft.com/40f647ba-05ed-453a-8eea-729b2f59ac05">FaxDevStartJob</a> function.


### -param CallHandle [in]

Type: <b>HCALL</b>

Specifies a call handle returned by the TAPI 2.x <a href="https://msdn.microsoft.com/7b24e3c3-bc69-488b-a698-cf17875bc3c5">LINE_CALLSTATE</a> message.


### -param Reserved1 [in]

Type: <b>DWORD</b>

This parameter is reserved for future use by Microsoft. It must be set to zero.


### -param Reserved2 [in]

Type: <b>DWORD</b>

This parameter is reserved for future use by Microsoft. It must be set to zero.


## -returns



Type: <b>BOOL</b>

The fax service returns a value of <b>TRUE</b> to indicate that the active fax operation should continue.

The fax service returns a value of <b>FALSE</b> to indicate that the active fax operation should be terminated. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <i>FaxSendCallback</i> callback function provides the fax service with the <i>CallHandle</i> that TAPI assigns. This handle is necessary for TAPI message routing. If the FSP does not call <i>FaxSendCallback</i>, it will miss all further call events.

A virtual FSP does not need the <i>FaxSendCallback</i> function.




## -see-also




<a href="https://msdn.microsoft.com/402583fd-aef8-4197-a41e-870825c58351">Fax Service Provider Functions</a>



<a href="https://msdn.microsoft.com/9ec25812-658f-4d64-85c4-8ab66be5d93e">FaxDevSend</a>



<a href="https://msdn.microsoft.com/40f647ba-05ed-453a-8eea-729b2f59ac05">FaxDevStartJob</a>



<a href="https://msdn.microsoft.com/7b24e3c3-bc69-488b-a698-cf17875bc3c5">LINE_CALLSTATE</a>



<a href="https://msdn.microsoft.com/a8788e8a-e97c-4082-8e89-b6f4a7568d3a">Using the Fax Service Provider API</a>
 

 

