---
UID: NF:photoacquire.IPhotoAcquireSource.GetDeviceId
title: IPhotoAcquireSource::GetDeviceId (photoacquire.h)
description: The GetDeviceId method retrieves the identifier (ID) of the device.
helpviewer_keywords: ["GetDeviceId","GetDeviceId method [Picture Acquisition]","GetDeviceId method [Picture Acquisition]","IPhotoAcquireSource interface","IPhotoAcquireSource interface [Picture Acquisition]","GetDeviceId method","IPhotoAcquireSource.GetDeviceId","IPhotoAcquireSource::GetDeviceId","IPhotoAcquireSourceGetDeviceId","photoacquire/IPhotoAcquireSource::GetDeviceId","picacq.iphotoacquiresource_getdeviceid"]
old-location: picacq\iphotoacquiresource_getdeviceid.htm
tech.root: picacq
ms.assetid: 4c997e76-9109-403f-821f-d73e8577b1ac
ms.date: 12/05/2018
ms.keywords: GetDeviceId, GetDeviceId method [Picture Acquisition], GetDeviceId method [Picture Acquisition],IPhotoAcquireSource interface, IPhotoAcquireSource interface [Picture Acquisition],GetDeviceId method, IPhotoAcquireSource.GetDeviceId, IPhotoAcquireSource::GetDeviceId, IPhotoAcquireSourceGetDeviceId, photoacquire/IPhotoAcquireSource::GetDeviceId, picacq.iphotoacquiresource_getdeviceid
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPhotoAcquireSource::GetDeviceId
 - photoacquire/IPhotoAcquireSource::GetDeviceId
dev_langs:
 - c++
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

<a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresource-getdeviceicons">GetDeviceIcons</a>



<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquiresource">IPhotoAcquireSource Interface</a>