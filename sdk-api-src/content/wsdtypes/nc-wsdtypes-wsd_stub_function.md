---
UID: NC:wsdtypes.WSD_STUB_FUNCTION
title: WSD_STUB_FUNCTION (wsdtypes.h)
author: windows-sdk-content
description: Describes a stub function used to handle an incoming message.
old-location: ncd\wsd_stub_function_func.htm
tech.root: WsdApi
ms.assetid: 39d16b22-2af0-43e4-a0d2-ca5e1d3a9434
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WSD_STUB_FUNCTION, WSD_STUB_FUNCTION callback, WSD_STUB_FUNCTION callback function, ncd.wsd_stub_function_func, wsdtypes/WSD_STUB_FUNCTION
ms.topic: callback
f1_keywords:
- wsdtypes/WSD_STUB_FUNCTION
dev_langs:
 - c++
req.header: wsdtypes.h
req.include-header: Wsdapi.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- WsdTypes.h
api_name:
- WSD_STUB_FUNCTION
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WSD_STUB_FUNCTION callback function


## -description


Describes a stub function used to handle an incoming message. This function should only be implemented in and used by <a href="https://docs.microsoft.com/windows/desktop/WsdApi/web-services-for-devices-code-generator">generated code</a>.


## -parameters




### -param *server

Pointer to the service object that was registered as a handler for messages of this type. Service objects are registered by calling one of the following methods:  <a href="https://docs.microsoft.com/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-registerservice">IWSDDeviceHost::RegisterService</a>, <a href="https://docs.microsoft.com/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-adddynamicservice">IWSDDeviceHost::AddDynamicService</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdserviceproxy-subscribetooperation">IWSDServiceProxy::SubscribeToOperation</a>.


### -param *session

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/wsdhost/nn-wsdhost-iwsdservicemessaging">IWSDServiceMessaging</a> object used for sending a fault or message response.


### -param *event

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_event">WSD_EVENT</a> structure that contains the data for the current request.


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
 



