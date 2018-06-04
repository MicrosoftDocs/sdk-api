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

# _ACTRL_PROPERTY_ENTRYA structure


## -description


Contains a list of access-control entries for an object or a specified property on an object.



## -struct-fields




### -field lpProperty

The GUID of a property on an object. Use the <a href="https://msdn.microsoft.com/49235b28-a0c5-4f69-9932-85350d7bcbb8">UuidToString</a> function to generate a string representation of a property GUID.


### -field pAccessEntryList

A pointer to an <a href="https://msdn.microsoft.com/d0e71756-0247-4c6b-b8b5-a343121b7406">ACTRL_ACCESS_ENTRY_LIST</a> structure that contains a list of access-control entries.


### -field fListFlags

Flags that specify information about the <b>pProperty</b> property. This member can be 0 or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ACTRL_ACCESS_PROTECTED_"></a><a id="actrl_access_protected_"></a><dl>
<dt><b>ACTRL_ACCESS_PROTECTED
</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Protects the object or property from inheriting access-control entries.


</td>
</tr>
</table>
 


## -remarks



To create an <b>ACTRL_PROPERTY_ENTRY</b> structure that grants everyone full access to an object, set the <b>pAccessEntryList</b> member to <b>NULL</b>. 



To create an <b>ACTRL_PROPERTY_ENTRY</b> structure that denies all access to an object, set the <b>pAccessEntryList</b> member to point to an <a href="https://msdn.microsoft.com/d0e71756-0247-4c6b-b8b5-a343121b7406">ACTRL_ACCESS_ENTRY_LIST</a> structure whose <b>cEntries</b> member is 0 and <b>pAccessList</b> member is <b>NULL</b>. 




## -see-also




<a href="https://msdn.microsoft.com/d0e71756-0247-4c6b-b8b5-a343121b7406">ACTRL_ACCESS_ENTRY_LIST</a>



<a href="https://msdn.microsoft.com/49235b28-a0c5-4f69-9932-85350d7bcbb8">UuidToString</a>
 

 

