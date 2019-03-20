---
UID: NF:portabledeviceapi.IPortableDeviceService.Advise
title: IPortableDeviceService::Advise (portabledeviceapi.h)
author: windows-sdk-content
description: Registers an application-defined callback object that receives service events.
old-location: wpdsdk\iportabledeviceservice_advise.htm
tech.root: wpd_sdk
ms.assetid: 128b1ee9-fd1f-4480-ae9a-b1d0bc86cf1b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Advise, Advise method [Windows Portable Devices SDK], Advise method [Windows Portable Devices SDK],IPortableDeviceService interface, IPortableDeviceService interface [Windows Portable Devices SDK],Advise method, IPortableDeviceService.Advise, IPortableDeviceService::Advise, portabledeviceapi/IPortableDeviceService::Advise, wpdsdk.iportabledeviceservice_advise
ms.topic: method
req.header: portabledeviceapi.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceAPI.h
api_name:
 - IPortableDeviceService.Advise
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPortableDeviceService::Advise


## -description


The <b>Advise</b> method registers an application-defined callback object that receives service events.


## -parameters




### -param dwFlags [in]

Not used.


### -param pCallback [in]

The  <a href="https://msdn.microsoft.com/1fb2d5d8-82b8-4c51-a086-bdcad33da190">IPortableDeviceEventCallback</a> interface specifying the callback object to register.


### -param pParameters [in]

The <a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues</a> interface specifying the event-registration parameters, or <b>NULL</b> if the callback object is to receive all service events.


### -param ppszCookie [out]

The unique context ID for the callback object. This value matches that used by the <a href="https://msdn.microsoft.com/4982efa9-82f2-457b-acf4-c6f7d48cf6f7">Unadvise</a> method to unregister the callback object.


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
A <b>NULL</b> value was specified for the <i>pCallback</i> parameter or the <i>ppszCookie</i> parameter.

</td>
</tr>
</table>
 




## -remarks



During cleanup, an application should unregister the callback object by calling the <a href="https://msdn.microsoft.com/4982efa9-82f2-457b-acf4-c6f7d48cf6f7">Unadvise</a> method, and then release the memory referenced by the <i>ppszCookie</i> parameter by calling the <b>CoTaskMemFree</b> function.




## -see-also




<a href="https://msdn.microsoft.com/f57344d5-c978-4c27-b8a9-b42492bd9312">IPortableDeviceService Interface</a>
 

 

