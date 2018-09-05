---
UID: NF:portabledeviceapi.IPortableDeviceService.Methods
title: IPortableDeviceService::Methods
author: windows-sdk-content
description: Retrieves the IPortableDeviceServiceMethods interface that is used to invoke custom functionality on the service.
old-location: wpdsdk\iportabledeviceservice_methods.htm
old-project: wpd_sdk
ms.assetid: 345102d4-3dac-4878-9196-bb0d97c0df07
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IPortableDeviceService interface [Windows Portable Devices SDK],Methods method, IPortableDeviceService.Methods, IPortableDeviceService::Methods, Methods, Methods method [Windows Portable Devices SDK], Methods method [Windows Portable Devices SDK],IPortableDeviceService interface, portabledeviceapi/IPortableDeviceService::Methods, wpdsdk.iportabledeviceservice_methods
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: portabledeviceapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: PortableDeviceAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceAPI.h
api_name:
 - IPortableDeviceService.Methods
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPortableDeviceService::Methods


## -description


The <b>Methods</b> method retrieves the <a href="https://msdn.microsoft.com/9d233dea-91b6-4358-830c-6abe466264e5">IPortableDeviceServiceMethods</a> interface that is used to invoke custom functionality on the service.


## -parameters




### -param ppMethods [out]

The <a href="https://msdn.microsoft.com/9d233dea-91b6-4358-830c-6abe466264e5">IPortableDeviceServiceMethods</a> interface used for invoking methods on the given service.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A <b>NULL</b> parameter was specified.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f57344d5-c978-4c27-b8a9-b42492bd9312">IPortableDeviceService Interface</a>



<a href="https://msdn.microsoft.com/3a2796c8-1a39-49eb-98e1-c9e06c61f397">Invoking Service Methods</a>



<a href="https://msdn.microsoft.com/d3072e34-65f2-4eeb-bcfa-e2db2d34e680">Invoking Service Methods Asynchronously</a>
 

 

