---
UID: NF:photoacquire.IPhotoAcquireProgressCB.EndEnumeration
title: IPhotoAcquireProgressCB::EndEnumeration (photoacquire.h)
description: The EndEnumeration method provides extended functionality when enumeration of files from the image source is complete. The application provides the implementation of the EndEnumeration method.
helpviewer_keywords: ["EndEnumeration","EndEnumeration method [Picture Acquisition]","EndEnumeration method [Picture Acquisition]","IPhotoAcquireProgressCB interface","IPhotoAcquireProgressCB interface [Picture Acquisition]","EndEnumeration method","IPhotoAcquireProgressCB.EndEnumeration","IPhotoAcquireProgressCB::EndEnumeration","IPhotoAcquireProgressCBEndEnumeration","photoacquire/IPhotoAcquireProgressCB::EndEnumeration","picacq.iphotoacquireprogresscb_endenumeration"]
old-location: picacq\iphotoacquireprogresscb_endenumeration.htm
tech.root: picacq
ms.assetid: dac16ca2-bd80-4771-9e81-09d07958a4bb
ms.date: 12/05/2018
ms.keywords: EndEnumeration, EndEnumeration method [Picture Acquisition], EndEnumeration method [Picture Acquisition],IPhotoAcquireProgressCB interface, IPhotoAcquireProgressCB interface [Picture Acquisition],EndEnumeration method, IPhotoAcquireProgressCB.EndEnumeration, IPhotoAcquireProgressCB::EndEnumeration, IPhotoAcquireProgressCBEndEnumeration, photoacquire/IPhotoAcquireProgressCB::EndEnumeration, picacq.iphotoacquireprogresscb_endenumeration
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
 - IPhotoAcquireProgressCB::EndEnumeration
 - photoacquire/IPhotoAcquireProgressCB::EndEnumeration
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
 - IPhotoAcquireProgressCB.EndEnumeration
---

# IPhotoAcquireProgressCB::EndEnumeration


## -description

The <code>EndEnumeration</code> method provides extended functionality when enumeration of files from the image source is complete. The application provides the implementation of the <code>EndEnumeration</code> method.

## -parameters

### -param hr [in]

Specifies the result of the enumeration operation.

## -returns

The method returns an <b>HRESULT</b>. Your implementation is not limited to the following return values. Any failing HRESULT other than E_NOTIMPL is fatal and will cause the transfer to abort.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The method is not yet implemented

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireprogresscb">IPhotoAcquireProgressCB Interface</a>