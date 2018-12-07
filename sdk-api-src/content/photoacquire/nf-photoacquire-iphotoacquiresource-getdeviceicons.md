---
UID: NF:photoacquire.IPhotoAcquireSource.GetDeviceIcons
title: IPhotoAcquireSource::GetDeviceIcons
author: windows-sdk-content
description: The GetDeviceIcons method retrieves the icons that are used to represent the device.
old-location: picacq\iphotoacquiresource_getdeviceicons.htm
tech.root: acquisition
ms.assetid: 98859baa-a6bd-4b12-992b-af6736fa9650
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDeviceIcons, GetDeviceIcons method [Picture Acquisition], GetDeviceIcons method [Picture Acquisition],IPhotoAcquireSource interface, IPhotoAcquireSource interface [Picture Acquisition],GetDeviceIcons method, IPhotoAcquireSource.GetDeviceIcons, IPhotoAcquireSource::GetDeviceIcons, IPhotoAcquireSourceGetDeviceIcons, photoacquire/IPhotoAcquireSource::GetDeviceIcons, picacq.iphotoacquiresource_getdeviceicons
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: photoacquire.h
req.include-header: 
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
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PhotoAcquireUID.lib
 - PhotoAcquireUID.dll
api_name:
 - IPhotoAcquireSource.GetDeviceIcons
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPhotoAcquireSource::GetDeviceIcons


## -description



The <code>GetDeviceIcons</code> method retrieves the icons that are used to represent the device.




## -parameters




### -param nSize [in]

Integer value containing the size of the icon to retrieve.


### -param phLargeIcon [out]

Specifies the large icon used for the device.


### -param phSmallIcon [out]

Specifies the small icon used for the device.


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
A null pointer was passed where non-null was expected.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/4c997e76-9109-403f-821f-d73e8577b1ac">GetDeviceId</a>



<a href="https://msdn.microsoft.com/6671d550-8c12-40e3-bf6f-33203e69cff0">IPhotoAcquireSource Interface</a>
 

 

