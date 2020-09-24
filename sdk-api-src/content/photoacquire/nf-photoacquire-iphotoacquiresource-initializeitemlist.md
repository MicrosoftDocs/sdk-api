---
UID: NF:photoacquire.IPhotoAcquireSource.InitializeItemList
title: IPhotoAcquireSource::InitializeItemList (photoacquire.h)
description: The InitializeItemList method enumerates transferable items on the device and passes each item to the optional progress callback, if it is supplied.
helpviewer_keywords: ["IPhotoAcquireSource interface [Picture Acquisition]","InitializeItemList method","IPhotoAcquireSource.InitializeItemList","IPhotoAcquireSource::InitializeItemList","IPhotoAcquireSourceInitializeItemList","InitializeItemList","InitializeItemList method [Picture Acquisition]","InitializeItemList method [Picture Acquisition]","IPhotoAcquireSource interface","photoacquire/IPhotoAcquireSource::InitializeItemList","picacq.iphotoacquiresource_initializeitemlist"]
old-location: picacq\iphotoacquiresource_initializeitemlist.htm
tech.root: picacq
ms.assetid: 1e0ebbc7-888d-4044-8257-47c1719cf7fc
ms.date: 12/05/2018
ms.keywords: IPhotoAcquireSource interface [Picture Acquisition],InitializeItemList method, IPhotoAcquireSource.InitializeItemList, IPhotoAcquireSource::InitializeItemList, IPhotoAcquireSourceInitializeItemList, InitializeItemList, InitializeItemList method [Picture Acquisition], InitializeItemList method [Picture Acquisition],IPhotoAcquireSource interface, photoacquire/IPhotoAcquireSource::InitializeItemList, picacq.iphotoacquiresource_initializeitemlist
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
 - IPhotoAcquireSource::InitializeItemList
 - photoacquire/IPhotoAcquireSource::InitializeItemList
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
 - IPhotoAcquireSource.InitializeItemList
---

# IPhotoAcquireSource::InitializeItemList


## -description

The <code>InitializeItemList</code> method enumerates transferable items on the device and passes each item to the optional progress callback, if it is supplied.

## -parameters

### -param fForceEnumeration [in]

Flag that, if set to <b>TRUE</b>, indicates that enumeration will be repeated even if the item list has already been initialized. If set to <b>FALSE</b>, this flag indicates that repeated calls to <code>InitializeItemList</code> after the item list has already been initialized will not enumerate items again.

### -param pPhotoAcquireProgressCB [in]

Optional. Pointer to an <a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireprogresscb">IPhotoAcquireProgressCB</a> object.

### -param pnItemCount [out]

Returns the number of items found.

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

If <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquire-acquire">IPhotoAcquire::Acquire</a> is called without first calling <code>InitializeItemList</code>, initialization of the item list is done implicitly.

The first time the item list is initialized—either implicitly through <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquire-acquire">IPhotoAcquire::Acquire</a> or explicitly by calling <code>InitializeItemList</code>—each item is enumerated. During enumeration, if an <a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireprogresscb">IPhotoAcquireProgressCB</a> object is passed to <code>InitializeItemList</code>, its implementation of <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-startenumeration">StartEnumeration</a>, <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-founditem">FoundItem</a>, and <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-endenumeration">EndEnumeration</a> may be used to apply further filtering or control to the list of items to be transferred.

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquire">IPhotoAcquire Interface</a>



<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireprogresscb">IPhotoAcquireProgressCB Interface</a>



<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquiresource">IPhotoAcquireSource Interface</a>