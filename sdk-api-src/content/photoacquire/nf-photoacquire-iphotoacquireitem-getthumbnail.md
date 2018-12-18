---
UID: NF:photoacquire.IPhotoAcquireItem.GetThumbnail
title: IPhotoAcquireItem::GetThumbnail
author: windows-sdk-content
description: The GetThumbnail method retrieves the thumbnail provided for an item.
old-location: picacq\iphotoacquireitem_getthumbnail.htm
tech.root: acquisition
ms.assetid: a347dc8b-7e95-4830-b848-ac3e7d495b3b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetThumbnail, GetThumbnail method [Picture Acquisition], GetThumbnail method [Picture Acquisition],IPhotoAcquireItem interface, IPhotoAcquireItem interface [Picture Acquisition],GetThumbnail method, IPhotoAcquireItem.GetThumbnail, IPhotoAcquireItem::GetThumbnail, IPhotoAcquireItemGetThumbnail, photoacquire/IPhotoAcquireItem::GetThumbnail, picacq.iphotoacquireitem_getthumbnail
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
 - IPhotoAcquireItem.GetThumbnail
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPhotoAcquireItem::GetThumbnail


## -description



The <code>GetThumbnail</code> method retrieves the thumbnail provided for an item.




## -parameters




### -param sizeThumbnail [in]

Specifies the size of the thumbnail.


### -param phbmpThumbnail [out]

Specifies a handle to the thumbnail bitmap.


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
 

 

