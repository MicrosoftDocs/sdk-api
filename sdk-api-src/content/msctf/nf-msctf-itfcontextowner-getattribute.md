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

# ITfContextOwner::GetAttribute


## -description


The <b>ITfContextOwner::GetAttribute</b> method returns the value of a supported attribute. If the attribute is unsupported, the <i>pvarValue</i> parameter is set to VT_EMPTY.


## -parameters




### -param rguidAttribute [in]

Specifies the attribute GUID.


### -param pvarValue [out]

Receives the attribute value. If the attribute is unsupported, this parameter is set to VT_EMPTY.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>
 




## -remarks



Context owners using the default text store of the TSF manager can implement a simplified version of attributes with this method. The supported attributes are application or text service dependent. For more information about predefined attributes recognized in TSF, see the following topics.




## -see-also




<a href="https://msdn.microsoft.com/630646df-dd47-4dbf-9787-f9d697ad8d7a">ITfContextOwner</a>



<a href="https://msdn.microsoft.com/8536938b-98a1-415b-b5f2-45b90215c270">Other Predefined Attributes</a>



<a href="https://msdn.microsoft.com/8d73c258-77d5-46db-9d31-ac41d9e7acb3">Predefined Font Attributes</a>



<a href="https://msdn.microsoft.com/9a9e1912-51c0-40e0-9e3a-b84ea7077dbe">Predefined List Attributes</a>



<a href="https://msdn.microsoft.com/af73edb8-b706-40e4-a093-4ac22d33ecdc">Predefined Text Attributes</a>
 

 

