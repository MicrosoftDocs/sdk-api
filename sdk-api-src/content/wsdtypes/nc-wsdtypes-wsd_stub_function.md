---
UID: NC:wsdtypes.WSD_STUB_FUNCTION
title: WSD_STUB_FUNCTION
author: windows-sdk-content
description: Describes a stub function used to handle an incoming message.
old-location: ncd\wsd_stub_function_func.htm
old-project: wsdapi
ms.assetid: 39d16b22-2af0-43e4-a0d2-ca5e1d3a9434
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WSD_STUB_FUNCTION, WSD_STUB_FUNCTION callback, WSD_STUB_FUNCTION callback function, ncd.wsd_stub_function_func, wsdtypes/WSD_STUB_FUNCTION
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: wsdtypes.h
req.include-header: Wsdapi.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WsdTypes.h
api_name:
 - WSD_STUB_FUNCTION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSD_STUB_FUNCTION callback function


## -description


Describes a stub function used to handle an incoming message. This function should only be implemented in and used by <a href="https://msdn.microsoft.com/76dffca8-bb84-4384-a9e8-120a4cf2acac">generated code</a>.


## -parameters




### -param *server

Pointer to the service object that was registered as a handler for messages of this type. Service objects are registered by calling one of the following methods:  <a href="https://msdn.microsoft.com/8e125e72-4060-4be6-b370-b2f6b24d9da7">IWSDDeviceHost::RegisterService</a>, <a href="https://msdn.microsoft.com/0ef7760d-39eb-48fe-a7e9-043c2b9ba5a4">IWSDDeviceHost::AddDynamicService</a>, or <a href="https://msdn.microsoft.com/d3294bd7-f3df-4571-92f6-eb6bc57240fb">IWSDServiceProxy::SubscribeToOperation</a>.


### -param *session

Pointer to an <a href="https://msdn.microsoft.com/06584474-1c55-43db-9c7a-fefea8d16eed">IWSDServiceMessaging</a> object used for sending a fault or message response.


### -param *event

Pointer to a <a href="https://msdn.microsoft.com/d8697474-bfe5-4704-b1ac-15cf96f2ca92">WSD_EVENT</a> structure that contains the data for the current request.


## -returns



Possible return values include, but are not limited to, the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 



