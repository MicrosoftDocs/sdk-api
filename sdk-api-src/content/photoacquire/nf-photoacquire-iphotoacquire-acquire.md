---
UID: NF:photoacquire.IPhotoAcquire.Acquire
title: IPhotoAcquire::Acquire (photoacquire.h)
description: The Acquire method acquires photos from a device.
helpviewer_keywords: ["Acquire","Acquire method [Picture Acquisition]","Acquire method [Picture Acquisition]","IPhotoAcquire interface","IPhotoAcquire interface [Picture Acquisition]","Acquire method","IPhotoAcquire.Acquire","IPhotoAcquire::Acquire","IPhotoAcquireAcquire","photoacquire/IPhotoAcquire::Acquire","picacq.iphotoacquire_acquire"]
old-location: picacq\iphotoacquire_acquire.htm
tech.root: picacq
ms.assetid: 1000511f-40a6-4d5e-a55f-97e25f6c1e11
ms.date: 12/05/2018
ms.keywords: Acquire, Acquire method [Picture Acquisition], Acquire method [Picture Acquisition],IPhotoAcquire interface, IPhotoAcquire interface [Picture Acquisition],Acquire method, IPhotoAcquire.Acquire, IPhotoAcquire::Acquire, IPhotoAcquireAcquire, photoacquire/IPhotoAcquire::Acquire, picacq.iphotoacquire_acquire
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
 - IPhotoAcquire::Acquire
 - photoacquire/IPhotoAcquire::Acquire
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
 - IPhotoAcquire.Acquire
---

# IPhotoAcquire::Acquire


## -description

The <code>Acquire</code> method acquires photos from a device.

## -parameters

### -param pPhotoAcquireSource [in]

Pointer to an <a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquiresource">IPhotoAcquireSource</a> object representing the device from which to acquire photos. Initialize this object by calling <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquire-createphotosource">CreatePhotoSource</a>.

### -param fShowProgress [in]

Flag that, when set to <b>TRUE</b>, indicates that a progress dialog will be shown.

### -param hWndParent [in]

Handle to a parent window.

### -param pszApplicationName [in]

Pointer to a null-terminated string containing the application name.

### -param pPhotoAcquireProgressCB [in]

Pointer to an optional <a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireprogresscb">IPhotoAcquireProgressCB</a> object.

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
Non-<b>NULL</b> pointer was expected.

</td>
</tr>
</table>

## -remarks

To initialize the <i>pPhotoAcquireSource</i> parameter passed to <code>Acquire</code>, <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquire-createphotosource">CreatePhotoSource</a> should be called prior to calling <code>Acquire</code>.

<i>pPhotoAcquireProgressCB</i> provides callback methods that allow you to apply further filtering or control as items are acquired.

To verify that there are items in the device before acquisition, or to selectively acquire items from the device, call <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresource-initializeitemlist">IPhotoAcquireSource::InitializeItemList</a> to enumerate the items before calling <code>Acquire</code>.

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquire">IPhotoAcquire Interface</a>



<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireprogresscb">IPhotoAcquireProgressCB Interface</a>



<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquiresource">IPhotoAcquireSource Interface</a>