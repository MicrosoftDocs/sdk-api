---
UID: NF:photoacquire.IPhotoAcquireProgressCB.EndSession
title: IPhotoAcquireProgressCB::EndSession (photoacquire.h)
description: The EndSession method provides extended functionality when an acquisition session is completed. The application provides the implementation of the EndSession method.
helpviewer_keywords: ["EndSession","EndSession method [Picture Acquisition]","EndSession method [Picture Acquisition]","IPhotoAcquireProgressCB interface","IPhotoAcquireProgressCB interface [Picture Acquisition]","EndSession method","IPhotoAcquireProgressCB.EndSession","IPhotoAcquireProgressCB::EndSession","IPhotoAcquireProgressCBEndSession","photoacquire/IPhotoAcquireProgressCB::EndSession","picacq.iphotoacquireprogresscb_endsession"]
old-location: picacq\iphotoacquireprogresscb_endsession.htm
tech.root: picacq
ms.assetid: fb22709a-c1f8-4608-b984-46181e7c704e
ms.date: 12/05/2018
ms.keywords: EndSession, EndSession method [Picture Acquisition], EndSession method [Picture Acquisition],IPhotoAcquireProgressCB interface, IPhotoAcquireProgressCB interface [Picture Acquisition],EndSession method, IPhotoAcquireProgressCB.EndSession, IPhotoAcquireProgressCB::EndSession, IPhotoAcquireProgressCBEndSession, photoacquire/IPhotoAcquireProgressCB::EndSession, picacq.iphotoacquireprogresscb_endsession
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
 - IPhotoAcquireProgressCB::EndSession
 - photoacquire/IPhotoAcquireProgressCB::EndSession
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
 - IPhotoAcquireProgressCB.EndSession
---

# IPhotoAcquireProgressCB::EndSession


## -description

The <code>EndSession</code> method provides extended functionality when an acquisition session is completed. The application provides the implementation of the <code>EndSession</code> method.

## -parameters

### -param hr [in]

Specifies the result of the acquisition.

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