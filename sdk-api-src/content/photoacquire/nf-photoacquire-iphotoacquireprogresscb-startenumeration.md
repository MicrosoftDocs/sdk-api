---
UID: NF:photoacquire.IPhotoAcquireProgressCB.StartEnumeration
title: IPhotoAcquireProgressCB::StartEnumeration (photoacquire.h)
author: windows-sdk-content
description: The StartEnumeration method provides extended functionality when the enumeration of items to acquire begins.
old-location: picacq\iphotoacquireprogresscb_startenumeration.htm
tech.root: acquisition
ms.assetid: ef42722d-ca39-4d22-8de1-6b3926669abf
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPhotoAcquireProgressCB interface [Picture Acquisition],StartEnumeration method, IPhotoAcquireProgressCB.StartEnumeration, IPhotoAcquireProgressCB::StartEnumeration, IPhotoAcquireProgressCBStartEnumeration, StartEnumeration, StartEnumeration method [Picture Acquisition], StartEnumeration method [Picture Acquisition],IPhotoAcquireProgressCB interface, photoacquire/IPhotoAcquireProgressCB::StartEnumeration, picacq.iphotoacquireprogresscb_startenumeration
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
 - IPhotoAcquireProgressCB.StartEnumeration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPhotoAcquireProgressCB::StartEnumeration


## -description



The <code>StartEnumeration</code> method provides extended functionality when the enumeration of items to acquire begins.



The application provides the implementation of the <code>StartEnumeration</code> method.


## -parameters




### -param pPhotoAcquireSource [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquiresource">IPhotoAcquireSource</a> object that items are being enumerated from.


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
The method is not implemented.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireprogresscb">IPhotoAcquireProgressCB Interface</a>
 

 

