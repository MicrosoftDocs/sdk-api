---
UID: NF:portabledeviceapi.IPortableDeviceService.Unadvise
title: IPortableDeviceService::Unadvise (portabledeviceapi.h)
author: windows-sdk-content
description: Unregisters a service event callback object.
old-location: wpdsdk\iportabledeviceservice_unadvise.htm
tech.root: wpd_sdk
ms.assetid: 4982efa9-82f2-457b-acf4-c6f7d48cf6f7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPortableDeviceService interface [Windows Portable Devices SDK],Unadvise method, IPortableDeviceService.Unadvise, IPortableDeviceService::Unadvise, Unadvise, Unadvise method [Windows Portable Devices SDK], Unadvise method [Windows Portable Devices SDK],IPortableDeviceService interface, portabledeviceapi/IPortableDeviceService::Unadvise, wpdsdk.iportabledeviceservice_unadvise
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
 - IPortableDeviceService.Unadvise
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPortableDeviceService::Unadvise


## -description


The <b>Unadvise</b> method unregisters a service event callback object.


## -parameters




### -param pszCookie [in]

The unique context ID for the application-supplied callback object. This value matches that yielded by the <i>ppszCookie</i> parameter of the <a href="https://msdn.microsoft.com/128b1ee9-fd1f-4480-ae9a-b1d0bc86cf1b">Advise</a> method.


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
 

 

