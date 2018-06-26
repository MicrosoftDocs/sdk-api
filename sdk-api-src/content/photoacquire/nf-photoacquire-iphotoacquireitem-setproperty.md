---
UID: NF:photoacquire.IPhotoAcquireItem.SetProperty
title: IPhotoAcquireItem::SetProperty
author: windows-sdk-content
description: The SetProperty method sets a property for an item.
old-location: picacq\iphotoacquireitem_setproperty.htm
old-project: acquisition
ms.assetid: 24c8ee32-eb10-416f-81bd-ddccb0f81fd9
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IPhotoAcquireItem interface [Picture Acquisition],SetProperty method, IPhotoAcquireItem.SetProperty, IPhotoAcquireItem::SetProperty, IPhotoAcquireItemSetProperty, SetProperty, SetProperty method [Picture Acquisition], SetProperty method [Picture Acquisition],IPhotoAcquireItem interface, photoacquire/IPhotoAcquireItem::SetProperty, picacq.iphotoacquireitem_setproperty
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
 - IPhotoAcquireItem.SetProperty
product: Windows
targetos: Windows
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# IPhotoAcquireItem::SetProperty


## -description



The <code>SetProperty</code> method sets a property for an item.




## -parameters




### -param key [in]

Specifies a key for the property to set.


### -param pv [in]

Pointer to a property variant containing the value to set the property to.


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



The property is stored in memory, but is not written to the file.




## -see-also




<a href="https://msdn.microsoft.com/47ee6a23-5a0b-4f45-b278-9ebbeebf4fbb">GetProperty</a>



<a href="https://msdn.microsoft.com/57e099eb-bf8d-4465-af4d-fcfc3eee3b5b">IPhotoAcquireItem Interface</a>
 

 

