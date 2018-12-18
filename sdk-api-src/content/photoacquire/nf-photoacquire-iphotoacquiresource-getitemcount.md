---
UID: NF:photoacquire.IPhotoAcquireSource.GetItemCount
title: IPhotoAcquireSource::GetItemCount
author: windows-sdk-content
description: The GetItemCount method retrieves the number of items found by the InitializeItemList method.
old-location: picacq\iphotoacquiresource_getitemcount.htm
tech.root: acquisition
ms.assetid: f60538f2-f1b1-40bb-8663-ed93eede433e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetItemCount, GetItemCount method [Picture Acquisition], GetItemCount method [Picture Acquisition],IPhotoAcquireSource interface, IPhotoAcquireSource interface [Picture Acquisition],GetItemCount method, IPhotoAcquireSource.GetItemCount, IPhotoAcquireSource::GetItemCount, IPhotoAcquireSourceGetItemCount, photoacquire/IPhotoAcquireSource::GetItemCount, picacq.iphotoacquiresource_getitemcount
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
 - IPhotoAcquireSource.GetItemCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPhotoAcquireSource::GetItemCount


## -description



The <code>GetItemCount</code> method retrieves the number of items found by the <a href="https://msdn.microsoft.com/1e0ebbc7-888d-4044-8257-47c1719cf7fc">InitializeItemList</a> method.




## -parameters




### -param pnItemCount [out]

Pointer to an integer value containing the item count.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL was passed where a non-NULL pointer was expected.

</td>
</tr>
</table>
 




## -remarks



Before calling this method, call <a href="https://msdn.microsoft.com/1e0ebbc7-888d-4044-8257-47c1719cf7fc">InitializeItemList</a> to initialize the item list.




## -see-also




<a href="https://msdn.microsoft.com/6671d550-8c12-40e3-bf6f-33203e69cff0">IPhotoAcquireSource Interface</a>



<a href="https://msdn.microsoft.com/1e0ebbc7-888d-4044-8257-47c1719cf7fc">IPhotoAcquireSource::InitializeItemList</a>
 

 

