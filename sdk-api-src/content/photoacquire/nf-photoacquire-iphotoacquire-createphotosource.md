---
UID: NF:photoacquire.IPhotoAcquire.CreatePhotoSource
title: IPhotoAcquire::CreatePhotoSource (photoacquire.h)
description: The CreatePhotoSource method initializes an IPhotoAcquireSource object to pass to IPhotoAcquire::Acquire.
helpviewer_keywords: ["CreatePhotoSource","CreatePhotoSource method [Picture Acquisition]","CreatePhotoSource method [Picture Acquisition]","IPhotoAcquire interface","IPhotoAcquire interface [Picture Acquisition]","CreatePhotoSource method","IPhotoAcquire.CreatePhotoSource","IPhotoAcquire::CreatePhotoSource","IPhotoAcquireCreatePhotoSource","photoacquire/IPhotoAcquire::CreatePhotoSource","picacq.iphotoacquire_createphotosource"]
old-location: picacq\iphotoacquire_createphotosource.htm
tech.root: picacq
ms.assetid: 03dc14d4-03e8-4281-ae70-c9f2c5646694
ms.date: 12/05/2018
ms.keywords: CreatePhotoSource, CreatePhotoSource method [Picture Acquisition], CreatePhotoSource method [Picture Acquisition],IPhotoAcquire interface, IPhotoAcquire interface [Picture Acquisition],CreatePhotoSource method, IPhotoAcquire.CreatePhotoSource, IPhotoAcquire::CreatePhotoSource, IPhotoAcquireCreatePhotoSource, photoacquire/IPhotoAcquire::CreatePhotoSource, picacq.iphotoacquire_createphotosource
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
 - IPhotoAcquire::CreatePhotoSource
 - photoacquire/IPhotoAcquire::CreatePhotoSource
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
 - IPhotoAcquire.CreatePhotoSource
---

# IPhotoAcquire::CreatePhotoSource


## -description

The <code>CreatePhotoSource</code> method initializes an <a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquiresource">IPhotoAcquireSource</a> object to pass to <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquire-acquire">IPhotoAcquire::Acquire</a>.

## -parameters

### -param pszDevice [in]

Pointer to a null-terminated string containing the device name.

### -param ppPhotoAcquireSource [out]

Returns the initialized photo source to acquire photos from.

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
A non-<b>NULL</b> pointer was expected.

</td>
</tr>
</table>

## -remarks

The <a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquiresource">IPhotoAcquireSource</a> object created is used as the parameter for the <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquire-acquire">Acquire</a> method.

If an error occurs in <code>CreatePhotoSource</code>, <i>ppPhotoAcquireSource</i> is initialized to <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquire">IPhotoAcquire Interface</a>



<a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquire-acquire">IPhotoAcquire::Acquire</a>