---
UID: NF:photoacquire.IPhotoAcquireItem.GetProperty
title: IPhotoAcquireItem::GetProperty
author: windows-driver-content
description: The GetProperty method retrieves the value of a property of an item.
old-location: picacq\iphotoacquireitem_getproperty.htm
old-project: acquisition
ms.assetid: 47ee6a23-5a0b-4f45-b278-9ebbeebf4fbb
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetProperty, GetProperty method [Picture Acquisition], GetProperty method [Picture Acquisition],IPhotoAcquireItem interface, IPhotoAcquireItem interface [Picture Acquisition],GetProperty method, IPhotoAcquireItem.GetProperty, IPhotoAcquireItem::GetProperty, IPhotoAcquireItemGetProperty, photoacquire/IPhotoAcquireItem::GetProperty, picacq.iphotoacquireitem_getproperty
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
-	IPhotoAcquireItem.GetProperty
product: Windows
targetos: Windows
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPhotoAcquireItem::GetProperty


## -description



The <code>GetProperty</code> method retrieves the value of a property of an item.




## -parameters




### -param key [in]

Specifies a key for the property.


### -param pv [out]

Pointer to a property variant containing the property value.


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



For an item that is a shell object, this method will defer to the <b>IPropertyStore</b> object provided by the item if the property hasn't been set or updated using <a href="https://msdn.microsoft.com/24c8ee32-eb10-416f-81bd-ddccb0f81fd9">SetProperty</a>.




## -see-also




<a href="https://msdn.microsoft.com/57e099eb-bf8d-4465-af4d-fcfc3eee3b5b">IPhotoAcquireItem Interface</a>



<a href="https://msdn.microsoft.com/24c8ee32-eb10-416f-81bd-ddccb0f81fd9">SetProperty</a>
 

 

