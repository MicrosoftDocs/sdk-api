---
UID: NF:photoacquire.IPhotoAcquireProgressCB.EndItemDelete
title: IPhotoAcquireProgressCB::EndItemDelete
author: windows-sdk-content
description: The EndItemDelete method provides extended functionality each time a file is deleted from the image source. The application provides the implementation of the EndItemDelete method.
old-location: picacq\iphotoacquireprogresscb_enditemdelete.htm
tech.root: acquisition
ms.assetid: 2962b170-941f-4cf1-9969-4066ee0c57d9
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EndItemDelete, EndItemDelete method [Picture Acquisition], EndItemDelete method [Picture Acquisition],IPhotoAcquireProgressCB interface, IPhotoAcquireProgressCB interface [Picture Acquisition],EndItemDelete method, IPhotoAcquireProgressCB.EndItemDelete, IPhotoAcquireProgressCB::EndItemDelete, IPhotoAcquireProgressCBEndItemDelete, photoacquire/IPhotoAcquireProgressCB::EndItemDelete, picacq.iphotoacquireprogresscb_enditemdelete
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
 - IPhotoAcquireProgressCB.EndItemDelete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPhotoAcquireProgressCB::EndItemDelete


## -description



The <code>EndItemDelete</code> method provides extended functionality each time a file is deleted from the image source. The application provides the implementation of the <code>EndItemDelete</code> method.




## -parameters




### -param nItemIndex [in]

Integer value containing the item index.


### -param pPhotoAcquireItem [in]

Pointer to the deleted <a href="https://msdn.microsoft.com/57e099eb-bf8d-4465-af4d-fcfc3eee3b5b">IPhotoAcquireItem</a> object.


### -param hr [in]

Specifies the result of the delete operation.


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
This method is not yet implemented

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c4fcc470-1b05-4d33-8581-80c6e7488e04">IPhotoAcquireProgressCB Interface</a>
 

 

