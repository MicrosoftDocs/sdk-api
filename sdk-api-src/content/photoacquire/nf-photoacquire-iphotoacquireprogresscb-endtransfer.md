---
UID: NF:photoacquire.IPhotoAcquireProgressCB.EndTransfer
title: IPhotoAcquireProgressCB::EndTransfer (photoacquire.h)
author: windows-sdk-content
description: The EndTransfer method provides extended functionality when the transfer of all files is complete. The application provides the implementation of the EndTransfer method.
old-location: picacq\iphotoacquireprogresscb_endtransfer.htm
tech.root: acquisition
ms.assetid: 9e0fada0-6c83-4e82-a3ac-c5a4832f053f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EndTransfer, EndTransfer method [Picture Acquisition], EndTransfer method [Picture Acquisition],IPhotoAcquireProgressCB interface, IPhotoAcquireProgressCB interface [Picture Acquisition],EndTransfer method, IPhotoAcquireProgressCB.EndTransfer, IPhotoAcquireProgressCB::EndTransfer, IPhotoAcquireProgressCBEndTransfer, photoacquire/IPhotoAcquireProgressCB::EndTransfer, picacq.iphotoacquireprogresscb_endtransfer
ms.topic: method
f1_keywords: 
 - "photoacquire/IPhotoAcquireProgressCB.EndTransfer"
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
 - IPhotoAcquireProgressCB.EndTransfer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPhotoAcquireProgressCB::EndTransfer


## -description



The <code>EndTransfer</code> method provides extended functionality when the transfer of all files is complete. The application provides the implementation of the <code>EndTransfer</code> method.




## -parameters




### -param hr [in]

Specifies the result of the transfer.


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




<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireprogresscb">IPhotoAcquireProgressCB Interface</a>
 

 

