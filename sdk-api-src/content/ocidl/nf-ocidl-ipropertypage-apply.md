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

# IPropertyPage::Apply


## -description


Applies the current values to the underlying objects associated with the property page as previously passed to 
    <a href="https://msdn.microsoft.com/0d7a73ce-8e3c-40c5-9040-6370df5edc2b">IPropertyPage::SetObjects</a>.


## -parameters






## -returns



This method can return the standard return values <b>E_OUTOFMEMORY</b> and 
      <b>E_UNEXPECTED</b>, as well as the following values.

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
Changes were successfully applied and the property page is current with the underlying objects.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Changes were applied, but the property page cannot determine if its state is current with the 
        objects.

</td>
</tr>
</table>
 




## -remarks



The objects to be changed are provided through a previous call to 
     <a href="https://msdn.microsoft.com/0d7a73ce-8e3c-40c5-9040-6370df5edc2b">IPropertyPage::SetObjects</a>. By calling 
     <b>IPropertyPage::SetObjects</b> prior to calling this 
     method, the caller ensures that all underlying objects have the correct interfaces through which to communicate 
     changes. Therefore, this method should not fail because of non-existent interfaces.

After applying its values, the property page should determine if its state is now current with the objects in 
     order to properly implement 
     <a href="https://msdn.microsoft.com/6a19a659-8fab-4218-bc5a-c53860f578f6">IPropertyPage::IsPageDirty</a> and to provide both 
     <b>S_OK</b> and <b>S_FALSE</b> return values.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
E_NOTIMPL is not a valid return value.




## -see-also




<a href="https://msdn.microsoft.com/ad2cb3ae-dd24-4774-95bd-f5a0773c68b1">IPropertyPage</a>
 

 

