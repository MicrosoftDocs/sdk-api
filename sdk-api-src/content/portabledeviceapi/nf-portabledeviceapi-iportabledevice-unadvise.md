---
UID: NF:portabledeviceapi.IPortableDevice.Unadvise
title: IPortableDevice::Unadvise
author: windows-sdk-content
description: The Unadvise method unregisters a client from receiving callback notifications. You must call this method if you called Advise previously.
old-location: wpdsdk\iportabledevice_unadvise.htm
old-project: wpd_sdk
ms.assetid: 6720e92b-35cd-4e3f-bd21-36337cf80140
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IPortableDevice interface [Windows Portable Devices SDK],Unadvise method, IPortableDevice.Unadvise, IPortableDevice::Unadvise, IPortableDeviceUnadvise, Unadvise, Unadvise method [Windows Portable Devices SDK], Unadvise method [Windows Portable Devices SDK],IPortableDevice interface, portabledeviceapi/IPortableDevice::Unadvise, wpdsdk.iportabledevice_unadvise
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: portabledeviceapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
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
tech.root: 
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGUIDs.lib
 - PortableDeviceGUIDs.dll
api_name:
 - IPortableDevice.Unadvise
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# IPortableDevice::Unadvise


## -description


The <b>Unadvise</b> method unregisters a client from receiving callback notifications. You must call this method if you called <a href="https://msdn.microsoft.com/bab28a19-7ba2-4edd-b5aa-c2017b4bf8ca">Advise</a> previously.
      


## -parameters




### -param pszCookie [in]

Pointer to a null-terminated string that is a unique context ID. This was retrieved in the initial call to <a href="https://msdn.microsoft.com/bab28a19-7ba2-4edd-b5aa-c2017b4bf8ca">IPortableDevice::Advise</a>.
          


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/98c48e56-56b8-4800-b52b-ac08f2abf27e">IPortableDevice Interface</a>
 

 

