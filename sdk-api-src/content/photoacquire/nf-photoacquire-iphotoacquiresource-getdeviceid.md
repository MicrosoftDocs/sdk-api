---
UID: NF:photoacquire.IPhotoAcquireSource.GetDeviceId
title: IPhotoAcquireSource::GetDeviceId (photoacquire.h)
author: windows-sdk-content
description: The GetDeviceId method retrieves the identifier (ID) of the device.
old-location: picacq\iphotoacquiresource_getdeviceid.htm
tech.root: acquisition
ms.assetid: 4c997e76-9109-403f-821f-d73e8577b1ac
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDeviceId, GetDeviceId method [Picture Acquisition], GetDeviceId method [Picture Acquisition],IPhotoAcquireSource interface, IPhotoAcquireSource interface [Picture Acquisition],GetDeviceId method, IPhotoAcquireSource.GetDeviceId, IPhotoAcquireSource::GetDeviceId, IPhotoAcquireSourceGetDeviceId, photoacquire/IPhotoAcquireSource::GetDeviceId, picacq.iphotoacquiresource_getdeviceid
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
 - IPhotoAcquireSource.GetDeviceId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPhotoAcquireSource::GetDeviceId


## -description



The <code>GetDeviceId</code> method retrieves the identifier (ID) of the device.




## -parameters




### -param pbstrDeviceId [out]

Pointer to a string containing the device ID.


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




<a href="https://msdn.microsoft.com/98859baa-a6bd-4b12-992b-af6736fa9650">GetDeviceIcons</a>



<a href="https://msdn.microsoft.com/6671d550-8c12-40e3-bf6f-33203e69cff0">IPhotoAcquireSource Interface</a>
 

 

