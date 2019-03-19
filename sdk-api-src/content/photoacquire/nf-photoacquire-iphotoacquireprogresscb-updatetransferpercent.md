---
UID: NF:photoacquire.IPhotoAcquireProgressCB.UpdateTransferPercent
title: IPhotoAcquireProgressCB::UpdateTransferPercent (photoacquire.h)
author: windows-sdk-content
description: The UpdateTransferPercent method provides extended functionality when the percentage of items transferred changes. The application provides the implementation of the UpdateTransferPercent method.
old-location: picacq\iphotoacquireprogresscb_updatetransferpercent.htm
tech.root: acquisition
ms.assetid: a868663d-f926-4b29-9e1f-7df4ec36687b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPhotoAcquireProgressCB interface [Picture Acquisition],UpdateTransferPercent method, IPhotoAcquireProgressCB.UpdateTransferPercent, IPhotoAcquireProgressCB::UpdateTransferPercent, IPhotoAcquireProgressCBUpdateTransferPercent, UpdateTransferPercent, UpdateTransferPercent method [Picture Acquisition], UpdateTransferPercent method [Picture Acquisition],IPhotoAcquireProgressCB interface, photoacquire/IPhotoAcquireProgressCB::UpdateTransferPercent, picacq.iphotoacquireprogresscb_updatetransferpercent
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
 - IPhotoAcquireProgressCB.UpdateTransferPercent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPhotoAcquireProgressCB::UpdateTransferPercent


## -description



The <code>UpdateTransferPercent</code> method provides extended functionality when the percentage of items transferred changes. The application provides the implementation of the <code>UpdateTransferPercent</code> method.




## -parameters




### -param fOverall [in]

Flag that, when set to <b>TRUE</b>, indicates that the value contained in <i>nPercent</i> is a percentage of the overall transfer progress, rather than a percentage of an individual item's progress.


### -param nPercent [in]

Integer value containing the percentage of items transferred.


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
 

 

