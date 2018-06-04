---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IPropertyStore::SetValue


## -description


This method sets a property value or replaces or removes an existing value.


## -parameters




### -param key




### -param propvar






#### - Key

A reference to the PROPERTYKEY structure that is retrieved through <a href="https://msdn.microsoft.com/library/windows/hardware/ff536959">IPropertyStore::GetAt</a>. This structure contains a global unique identifier (GUID) for the property.


#### - pv

A pointer to a <a href="http://go.microsoft.com/fwlink/p/?linkid=106396">PROPVARIANT</a> structure that contains the new property data.


## -returns



The <code>IPropertyStore::SetValue</code> method can return any one of the following:

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
The property change was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INPLACE_S_TRUNCATED</b></dt>
</dl>
</td>
<td width="60%">
The value was set but truncated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
This is an error code. The property store was read-only so the method was not able to set the value.

</td>
</tr>
</table>
 




## -remarks



<code>IPropertyStore::SetValue</code> affects the current property store instance only. A property handler implements <code>IPropertyStore::SetValue</code> by accumulating property changes in an in-memory data structure. Property changes are written to the stream only when <a href="https://msdn.microsoft.com/library/windows/hardware/ff536957">IPropertyStore::Commit</a> is called.

If <b>IPropertyStore::Commit</b> is called on a read-only property store, the property handler determines this and returns STG_E_ACCESSDENIED.

If a value was added or removed as a result of <code>SetValue</code>, subsequent enumerations by <a href="https://msdn.microsoft.com/library/windows/hardware/ff536960">IPropertyStore::GetCount</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff536959">IPropertyStore::GetAt</a> reflect that change and subsequent calls to <code>IPropertyStore::SetValue</code> reflect the changed value.

<b>Adding a New Property</b>

If the property value that was pointed to by key does not exist in the store, <code>IPropertyStore::SetValue</code> adds the value to the store.

<b>Replacing an Existing Property Value</b>

If the property value that was pointed to by key already exists in the store, the stored value is replaced.

<b>Removing an Existing Property</b>

To remove a value from the property store, set the vt member of the structure that is pointed to by pv to VT_EMPTY. If that value is not present, do nothing and the method returns S_OK.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536957">IPropertyStore::Commit</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536959">IPropertyStore::GetAt</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536960">IPropertyStore::GetCount</a>
 

 

