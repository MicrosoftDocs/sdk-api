---
UID: NF:photoacquire.IPhotoAcquireProgressCB.StartItemTransfer
title: IPhotoAcquireProgressCB::StartItemTransfer
author: windows-sdk-content
description: The StartItemTransfer method provides extended functionality each time the transfer of an item begins. The application provides the implementation of the StartItemTransfer method.
old-location: picacq\iphotoacquireprogresscb_startitemtransfer.htm
tech.root: acquisition
ms.assetid: fffd9313-fbed-493b-a82e-1ccd202859c0
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IPhotoAcquireProgressCB interface [Picture Acquisition],StartItemTransfer method, IPhotoAcquireProgressCB.StartItemTransfer, IPhotoAcquireProgressCB::StartItemTransfer, IPhotoAcquireProgressCBStartItemTransfer, StartItemTransfer, StartItemTransfer method [Picture Acquisition], StartItemTransfer method [Picture Acquisition],IPhotoAcquireProgressCB interface, photoacquire/IPhotoAcquireProgressCB::StartItemTransfer, picacq.iphotoacquireprogresscb_startitemtransfer
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IPhotoAcquireProgressCB.StartItemTransfer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPhotoAcquireProgressCB::StartItemTransfer


## -description



The <code>StartItemTransfer</code> method provides extended functionality each time the transfer of an item begins. The application provides the implementation of the <code>StartItemTransfer</code> method.




## -parameters




### -param nItemIndex [in]

Integer value containing the item index in the list of items to transfer.


### -param pPhotoAcquireItem [in]

Pointer to the <a href="https://msdn.microsoft.com/57e099eb-bf8d-4465-af4d-fcfc3eee3b5b">IPhotoAcquireItem</a> object that is to be transferred.


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




<a href="https://msdn.microsoft.com/c4fcc470-1b05-4d33-8581-80c6e7488e04">IPhotoAcquireProgressCB Interface</a>
 

 

