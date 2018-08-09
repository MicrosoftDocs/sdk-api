---
UID: NF:photoacquire.IPhotoAcquireSource.GetItemAt
title: IPhotoAcquireSource::GetItemAt
author: windows-sdk-content
description: The GetItemAt method retrieves the IPhotoAcquireItem object at the given index in the list of items.
old-location: picacq\iphotoacquiresource_getitemat.htm
old-project: acquisition
ms.assetid: c066464b-1d88-4d43-8bfd-0f60f21db5fd
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetItemAt, GetItemAt method [Picture Acquisition], GetItemAt method [Picture Acquisition],IPhotoAcquireSource interface, IPhotoAcquireSource interface [Picture Acquisition],GetItemAt method, IPhotoAcquireSource.GetItemAt, IPhotoAcquireSource::GetItemAt, IPhotoAcquireSourceGetItemAt, photoacquire/IPhotoAcquireSource::GetItemAt, picacq.iphotoacquiresource_getitemat
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
tech.root: 
req.typenames: USER_INPUT_STRING_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PhotoAcquireUID.lib
 - PhotoAcquireUID.dll
api_name:
 - IPhotoAcquireSource.GetItemAt
product: Windows
targetos: Windows
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# IPhotoAcquireSource::GetItemAt


## -description



The <code>GetItemAt</code> method retrieves the <a href="https://msdn.microsoft.com/57e099eb-bf8d-4465-af4d-fcfc3eee3b5b">IPhotoAcquireItem</a> object at the given index in the list of items.




## -parameters




### -param nIndex [in]

Integer value containing the index.


### -param ppPhotoAcquireItem [out]

Pointer to the address of an <a href="https://msdn.microsoft.com/57e099eb-bf8d-4465-af4d-fcfc3eee3b5b">IPhotoAcquireItem</a> object.


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



Before calling this method, call <a href="https://msdn.microsoft.com/1e0ebbc7-888d-4044-8257-47c1719cf7fc">InitializeItemList</a> to initialize the item list.




## -see-also




<a href="https://msdn.microsoft.com/6671d550-8c12-40e3-bf6f-33203e69cff0">IPhotoAcquireSource Interface</a>
 

 

