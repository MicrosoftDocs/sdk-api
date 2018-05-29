---
UID: NF:photoacquire.IPhotoAcquireProgressCB.StartItemDelete
title: IPhotoAcquireProgressCB::StartItemDelete
author: windows-sdk-content
description: The StartItemDelete method provides extended functionality each time the deletion of an individual item from the device begins. The application provides the implementation of the StartItemDelete method.
old-location: picacq\iphotoacquireprogresscb_startitemdelete.htm
old-project: acquisition
ms.assetid: 0f4ab29d-ea9c-410d-94ab-4c4d8ed76b4d
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IPhotoAcquireProgressCB interface [Picture Acquisition],StartItemDelete method, IPhotoAcquireProgressCB.StartItemDelete, IPhotoAcquireProgressCB::StartItemDelete, IPhotoAcquireProgressCBStartItemDelete, StartItemDelete, StartItemDelete method [Picture Acquisition], StartItemDelete method [Picture Acquisition],IPhotoAcquireProgressCB interface, photoacquire/IPhotoAcquireProgressCB::StartItemDelete, picacq.iphotoacquireprogresscb_startitemdelete
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: USER_INPUT_STRING_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PhotoAcquireUID.lib
-	PhotoAcquireUID.dll
api_name:
-	IPhotoAcquireProgressCB.StartItemDelete
product: Windows
targetos: Windows
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPhotoAcquireProgressCB::StartItemDelete


## -description



The <code>StartItemDelete</code> method provides extended functionality each time the deletion of an individual item from the device begins. The application provides the implementation of the <code>StartItemDelete</code> method.




## -parameters




### -param nItemIndex [in]

Integer value containing the item index in the list of items to delete.


### -param pPhotoAcquireItem [in]

Pointer to the <a href="https://msdn.microsoft.com/57e099eb-bf8d-4465-af4d-fcfc3eee3b5b">IPhotoAcquireItem</a> object that is being deleted.


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
 

 

