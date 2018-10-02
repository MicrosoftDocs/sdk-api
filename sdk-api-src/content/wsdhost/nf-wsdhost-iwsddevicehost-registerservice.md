---
UID: NF:wsdhost.IWSDDeviceHost.RegisterService
title: IWSDDeviceHost::RegisterService
author: windows-sdk-content
description: Registers a service object for incoming requests and adds the service to the device host metadata.
old-location: ncd\iwsddevicehost_registerservice_method.htm
tech.root: WsdApi
ms.assetid: 8e125e72-4060-4be6-b370-b2f6b24d9da7
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWSDDeviceHost interface,RegisterService method, IWSDDeviceHost.RegisterService, IWSDDeviceHost::RegisterService, RegisterService, RegisterService method, RegisterService method,IWSDDeviceHost interface, ncd.iwsddevicehost_registerservice_method, wsdhost/IWSDDeviceHost::RegisterService
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wsdhost.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdHost.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDDeviceHost.RegisterService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDDeviceHost::RegisterService


## -description


Registers a service object for incoming requests and adds the service to the device host metadata.


## -parameters




### -param pszServiceId [in]

 The ID of the service to be registered. This ID must appear in the device's service host metadata. 



### -param pService [in]

The service object that will handle requests addressed to the specified service.



## -returns



Possible return values include, but are not limited to, the following:

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
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pszServiceId</i> is <b>NULL</b>, the length in characters of <i>pszServiceId</i> exceeds WSD_MAX_TEXT_LENGTH (8192), or a service matching <i>pszServiceId</i> has already been registered.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/497d0331-c88d-4381-8990-94227a9b9659">IWSDDeviceHost</a>
 

 

