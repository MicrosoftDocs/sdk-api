---
UID: NF:photoacquire.IPhotoAcquireItem.CanDelete
title: IPhotoAcquireItem::CanDelete
author: windows-sdk-content
description: The CanDelete method indicates whether an item may be deleted.
old-location: picacq\iphotoacquireitem_candelete.htm
tech.root: acquisition
ms.assetid: df0acbed-0352-4591-8908-f0dda1da25dd
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CanDelete, CanDelete method [Picture Acquisition], CanDelete method [Picture Acquisition],IPhotoAcquireItem interface, IPhotoAcquireItem interface [Picture Acquisition],CanDelete method, IPhotoAcquireItem.CanDelete, IPhotoAcquireItem::CanDelete, IPhotoAcquireItemCanDelete, photoacquire/IPhotoAcquireItem::CanDelete, picacq.iphotoacquireitem_candelete
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
 - IPhotoAcquireItem.CanDelete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPhotoAcquireItem::CanDelete


## -description



The <code>CanDelete</code> method indicates whether an item may be deleted.




## -parameters




### -param pfCanDelete [out]

Pointer to a flag that, when set to <b>TRUE</b>, indicates that the item can be deleted.


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
 




## -see-also




<a href="https://msdn.microsoft.com/57e099eb-bf8d-4465-af4d-fcfc3eee3b5b">IPhotoAcquireItem Interface</a>
 

 

