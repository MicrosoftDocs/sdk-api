---
UID: NF:photoacquire.IPhotoAcquireSource.GetPhotoAcquireSettings
title: IPhotoAcquireSource::GetPhotoAcquireSettings (photoacquire.h)
description: The GetPhotoAcquireSettings method obtains an IPhotoAcquireSettings object for working with acquisition settings.
helpviewer_keywords: ["GetPhotoAcquireSettings","GetPhotoAcquireSettings method [Picture Acquisition]","GetPhotoAcquireSettings method [Picture Acquisition]","IPhotoAcquireSource interface","IPhotoAcquireSource interface [Picture Acquisition]","GetPhotoAcquireSettings method","IPhotoAcquireSource.GetPhotoAcquireSettings","IPhotoAcquireSource::GetPhotoAcquireSettings","IPhotoAcquireSourceGetPhotoAcquireSettings","photoacquire/IPhotoAcquireSource::GetPhotoAcquireSettings","picacq.iphotoacquiresource_getphotoacquiresettings"]
old-location: picacq\iphotoacquiresource_getphotoacquiresettings.htm
tech.root: picacq
ms.assetid: b4c01856-b7e4-4318-aaf8-8e34e441ce75
ms.date: 12/05/2018
ms.keywords: GetPhotoAcquireSettings, GetPhotoAcquireSettings method [Picture Acquisition], GetPhotoAcquireSettings method [Picture Acquisition],IPhotoAcquireSource interface, IPhotoAcquireSource interface [Picture Acquisition],GetPhotoAcquireSettings method, IPhotoAcquireSource.GetPhotoAcquireSettings, IPhotoAcquireSource::GetPhotoAcquireSettings, IPhotoAcquireSourceGetPhotoAcquireSettings, photoacquire/IPhotoAcquireSource::GetPhotoAcquireSettings, picacq.iphotoacquiresource_getphotoacquiresettings
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
 - IPhotoAcquireSource::GetPhotoAcquireSettings
 - photoacquire/IPhotoAcquireSource::GetPhotoAcquireSettings
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
 - IPhotoAcquireSource.GetPhotoAcquireSettings
---

# IPhotoAcquireSource::GetPhotoAcquireSettings


## -description

The <code>GetPhotoAcquireSettings</code> method obtains an <a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquiresettings">IPhotoAcquireSettings</a> object for working with acquisition settings.

## -parameters

### -param ppPhotoAcquireSettings [out]

Pointer to the address of a photo acquire settings object.

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
Null value passed where non-null is expected.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquiresource">IPhotoAcquireSource Interface</a>