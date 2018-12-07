---
UID: NN:photoacquire.IPhotoAcquireItem
title: IPhotoAcquireItem
author: windows-sdk-content
description: The IPhotoAcquireItem interface provides methods for working with items as they are acquired from a device.
old-location: picacq\iphotoacquireitem.htm
tech.root: acquisition
ms.assetid: 57e099eb-bf8d-4465-af4d-fcfc3eee3b5b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPhotoAcquireItem, IPhotoAcquireItem interface [Picture Acquisition], IPhotoAcquireItem interface [Picture Acquisition],described, IPhotoAcquireItemInterface, photoacquire/IPhotoAcquireItem, picacq.iphotoacquireitem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - photoacquire.h
api_name:
 - IPhotoAcquireItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPhotoAcquireItem interface


## -description



The <code>IPhotoAcquireItem</code> interface provides methods for working with items as they are acquired from a device.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPhotoAcquireItem</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPhotoAcquireItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPhotoAcquireItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df0acbed-0352-4591-8908-f0dda1da25dd">CanDelete</a>
</td>
<td align="left" width="63%">
Indicates whether an item may be deleted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e1ffe49b-b7d6-46ae-b83b-8d8487bd7b24">Delete</a>
</td>
<td align="left" width="63%">
Deletes an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10048853-424b-4761-8a80-b1f674f856f4">GetItemName</a>
</td>
<td align="left" width="63%">
Retrieves the file name for an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/47ee6a23-5a0b-4f45-b278-9ebbeebf4fbb">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves the value of a property of an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0b138aa-42df-4bb6-905d-647b2289df58">GetStream</a>
</td>
<td align="left" width="63%">
Retrieves a read-only stream containing the contents of an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2fd410a0-20b5-4e16-9d36-89a14443c8bd">GetSubItemAt</a>
</td>
<td align="left" width="63%">
Retrieves the subitem of an item, given the index of the subitem.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2790d551-42ae-4009-998e-2579687203d6">GetSubItemCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of subitems contained in an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a347dc8b-7e95-4830-b848-ac3e7d495b3b">GetThumbnail</a>
</td>
<td align="left" width="63%">
Retrieves the thumbnail provided for an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24c8ee32-eb10-416f-81bd-ddccb0f81fd9">SetProperty</a>
</td>
<td align="left" width="63%">
Sets a property for an item.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f58529da-f419-445a-879a-2c087b770f0f">Interfaces</a>
 

 

