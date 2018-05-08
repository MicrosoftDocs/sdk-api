---
UID: NF:wsdhost.IWSDDeviceHost.RemoveDynamicService
title: IWSDDeviceHost::RemoveDynamicService
author: windows-driver-content
description: Unregisters a service object that was registered using AddDynamicService.
old-location: ncd\iwsddevicehost_removedynamicservice_method.htm
old-project: WsdApi
ms.assetid: 45c314d3-966b-4b90-ab23-fec2a8e4bc0f
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IWSDDeviceHost interface,RemoveDynamicService method, IWSDDeviceHost.RemoveDynamicService, IWSDDeviceHost::RemoveDynamicService, RemoveDynamicService, RemoveDynamicService method, RemoveDynamicService method,IWSDDeviceHost interface, ncd.iwsddevicehost_removedynamicservice_method, wsdhost/IWSDDeviceHost::RemoveDynamicService
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
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wsdapi.dll
api_name:
-	IWSDDeviceHost.RemoveDynamicService
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDDeviceHost::RemoveDynamicService


## -description


Unregisters a service object that was registered using <a href="https://msdn.microsoft.com/0ef7760d-39eb-48fe-a7e9-043c2b9ba5a4">AddDynamicService</a>. An unregistered service object does not receive incoming requests.


## -parameters




### -param pszServiceId [in]

The ID for the dynamic service to be removed.


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
<i>pszServiceId</i> is <b>NULL</b>, the length in characters of <i>pszServiceId</i> exceeds WSD_MAX_TEXT_LENGTH (8192), or <i>pszServiceId</i> was not found in the list of dynamic services.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed. It may have failed because the host has not been initialized. Call <a href="https://msdn.microsoft.com/library/windows/hardware/ff541624">Init</a> to initialize a device host.

</td>
</tr>
</table>
 




## -remarks



The device host releases its reference to the service object after the service is unregistered. The service object will not receive callbacks after <b>RemoveDynamicService</b> has completed.




## -see-also




<a href="https://msdn.microsoft.com/497d0331-c88d-4381-8990-94227a9b9659">IWSDDeviceHost</a>
 

 

