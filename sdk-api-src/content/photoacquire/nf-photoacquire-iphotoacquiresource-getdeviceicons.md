---
UID: NF:photoacquire.IPhotoAcquireSource.GetDeviceIcons
title: IPhotoAcquireSource::GetDeviceIcons (photoacquire.h)
description: The GetDeviceIcons method retrieves the icons that are used to represent the device.
helpviewer_keywords: ["GetDeviceIcons","GetDeviceIcons method [Picture Acquisition]","GetDeviceIcons method [Picture Acquisition]","IPhotoAcquireSource interface","IPhotoAcquireSource interface [Picture Acquisition]","GetDeviceIcons method","IPhotoAcquireSource.GetDeviceIcons","IPhotoAcquireSource::GetDeviceIcons","IPhotoAcquireSourceGetDeviceIcons","photoacquire/IPhotoAcquireSource::GetDeviceIcons","picacq.iphotoacquiresource_getdeviceicons"]
old-location: picacq\iphotoacquiresource_getdeviceicons.htm
tech.root: picacq
ms.assetid: 98859baa-a6bd-4b12-992b-af6736fa9650
ms.date: 12/05/2018
ms.keywords: GetDeviceIcons, GetDeviceIcons method [Picture Acquisition], GetDeviceIcons method [Picture Acquisition],IPhotoAcquireSource interface, IPhotoAcquireSource interface [Picture Acquisition],GetDeviceIcons method, IPhotoAcquireSource.GetDeviceIcons, IPhotoAcquireSource::GetDeviceIcons, IPhotoAcquireSourceGetDeviceIcons, photoacquire/IPhotoAcquireSource::GetDeviceIcons, picacq.iphotoacquiresource_getdeviceicons
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
 - IPhotoAcquireSource::GetDeviceIcons
 - photoacquire/IPhotoAcquireSource::GetDeviceIcons
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
 - IPhotoAcquireSource.GetDeviceIcons
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

<a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresource-getdeviceid">GetDeviceId</a>



<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquiresource">IPhotoAcquireSource Interface</a>