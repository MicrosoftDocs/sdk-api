---
UID: NF:photoacquire.IPhotoAcquireItem.GetStream
title: IPhotoAcquireItem::GetStream
author: windows-sdk-content
description: The GetStream method retrieves a read-only stream containing the contents of an item.
old-location: picacq\iphotoacquireitem_getstream.htm
tech.root: acquisition
ms.assetid: d0b138aa-42df-4bb6-905d-647b2289df58
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetStream, GetStream method [Picture Acquisition], GetStream method [Picture Acquisition],IPhotoAcquireItem interface, IPhotoAcquireItem interface [Picture Acquisition],GetStream method, IPhotoAcquireItem.GetStream, IPhotoAcquireItem::GetStream, IPhotoAcquireItemGetStream, photoacquire/IPhotoAcquireItem::GetStream, picacq.iphotoacquireitem_getstream
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
 - IPhotoAcquireItem.GetStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPhotoAcquireItem::GetStream


## -description



The <code>GetStream</code> method retrieves a read-only stream containing the contents of an item.




## -parameters




### -param ppStream [out]

Returns a stream object with the file contents.


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
 

 

