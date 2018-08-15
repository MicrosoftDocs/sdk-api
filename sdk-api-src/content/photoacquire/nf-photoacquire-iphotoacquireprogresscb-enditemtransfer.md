---
UID: NF:photoacquire.IPhotoAcquireProgressCB.EndItemTransfer
title: IPhotoAcquireProgressCB::EndItemTransfer
author: windows-sdk-content
description: The EndItemTransfer method provides extended functionality each time a file is transferred from the image source. The application provides the implementation of the EndItemTransfer method.
old-location: picacq\iphotoacquireprogresscb_enditemtransfer.htm
old-project: acquisition
ms.assetid: 8d2c0773-cb0b-4cc3-b61f-9ad4153bcf96
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: EndItemTransfer, EndItemTransfer method [Picture Acquisition], EndItemTransfer method [Picture Acquisition],IPhotoAcquireProgressCB interface, IPhotoAcquireProgressCB interface [Picture Acquisition],EndItemTransfer method, IPhotoAcquireProgressCB.EndItemTransfer, IPhotoAcquireProgressCB::EndItemTransfer, IPhotoAcquireProgressCBEndItemTransfer, photoacquire/IPhotoAcquireProgressCB::EndItemTransfer, picacq.iphotoacquireprogresscb_enditemtransfer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: photoacquire.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: USER_INPUT_STRING_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PhotoAcquireUID.lib
 - PhotoAcquireUID.dll
api_name:
 - IPhotoAcquireProgressCB.EndItemTransfer
product: Windows
targetos: Windows
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# IPhotoAcquireProgressCB::EndItemTransfer


## -description



The <code>EndItemTransfer</code> method provides extended functionality each time a file is transferred from the image source. The application provides the implementation of the <code>EndItemTransfer</code> method.




## -parameters




### -param nItemIndex [in]

Integer value containing the item index.


### -param pPhotoAcquireItem [in]

Pointer to a photo acquire item object.


### -param hr [in]

Specifies the result of the transfer operation.


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




<a href="https://msdn.microsoft.com/c4fcc470-1b05-4d33-8581-80c6e7488e04">IPhotoAcquireProgressCB Interface</a>
 

 

