---
UID: NF:portabledeviceapi.IPortableDeviceService.Capabilities
title: IPortableDeviceService::Capabilities
author: windows-sdk-content
description: Retrieves the service capabilities.
old-location: wpdsdk\iportabledeviceservice_capabilities.htm
old-project: wpd_sdk
ms.assetid: 62ef0c63-2908-458f-8e9f-eb6150441380
ms.author: windowssdkdev
ms.date: 04/12/2018
ms.keywords: Capabilities, Capabilities method [Windows Portable Devices SDK], Capabilities method [Windows Portable Devices SDK],IPortableDeviceService interface, IPortableDeviceService interface [Windows Portable Devices SDK],Capabilities method, IPortableDeviceService.Capabilities, IPortableDeviceService::Capabilities, portabledeviceapi/IPortableDeviceService::Capabilities, wpdsdk.iportabledeviceservice_capabilities
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
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
 - IPortableDeviceService.Capabilities
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPortableDeviceService::Capabilities


## -description


The <b>Capabilities</b> method retrieves the service capabilities.


## -parameters




### -param ppCapabilities [out]

The <a href="https://msdn.microsoft.com/d472d31c-90da-4ecc-9cf7-4474457a244f">IPortableDeviceServiceCapabilities</a> interface specifying the capabilities of the service.


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



<a href="https://msdn.microsoft.com/1bf3aa08-7ffc-417f-a67e-9eee042337b9">Retrieving Supported Service Events</a>



<a href="https://msdn.microsoft.com/b54dfeda-c2a3-42ec-895f-9abbbd4dd2ec">Retrieving Supported Service Formats</a>



<a href="https://msdn.microsoft.com/783a6552-9b22-4af4-9252-b443e2624687">Retrieving Supported Service Methods</a>
 

 

