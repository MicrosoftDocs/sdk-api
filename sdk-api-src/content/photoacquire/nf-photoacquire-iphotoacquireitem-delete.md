---
UID: NF:photoacquire.IPhotoAcquireItem.Delete
title: IPhotoAcquireItem::Delete
author: windows-sdk-content
description: The Delete method deletes an item.
old-location: picacq\iphotoacquireitem_delete.htm
tech.root: acquisition
ms.assetid: e1ffe49b-b7d6-46ae-b83b-8d8487bd7b24
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Delete, Delete method [Picture Acquisition], Delete method [Picture Acquisition],IPhotoAcquireItem interface, IPhotoAcquireItem interface [Picture Acquisition],Delete method, IPhotoAcquireItem.Delete, IPhotoAcquireItem::Delete, IPhotoAcquireItemDelete, photoacquire/IPhotoAcquireItem::Delete, picacq.iphotoacquireitem_delete
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
 - IPhotoAcquireItem.Delete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPhotoAcquireItem::Delete


## -description



The <code>Delete</code> method deletes an item.




## -parameters






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
</table>
 




## -remarks



To determine whether an item may be deleted, call <a href="https://msdn.microsoft.com/df0acbed-0352-4591-8908-f0dda1da25dd">CanDelete</a> first.




## -see-also




<a href="https://msdn.microsoft.com/57e099eb-bf8d-4465-af4d-fcfc3eee3b5b">IPhotoAcquireItem Interface</a>



<a href="https://msdn.microsoft.com/df0acbed-0352-4591-8908-f0dda1da25dd">IPhotoAcquireItem::CanDelete</a>
 

 

