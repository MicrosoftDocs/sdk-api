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

# ITfPropertyStore::GetPropertyRangeCreator


## -description




## -parameters




### -param pclsid [out]

Pointer to a <b>CLSID</b> that receives the class identifier of the registered text service that implements <a href="https://msdn.microsoft.com/f21619c5-5f59-4cc4-9f84-fa5f8a178d40">ITfCreatePropertyStore</a>. The method can return CLSID_NULL for this parameter if property store persistence is unsupported.


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



When the property store is unserialized, the TSF manager creates an object of this CLSID and obtains an <b>ITfCreatePropertyStore</b> interface pointer from it. The manager then uses the <b>ITfCreatePropertyStore</b> object to create the property store object.




## -see-also




<a href="https://msdn.microsoft.com/f21619c5-5f59-4cc4-9f84-fa5f8a178d40">ITfCreatePropertyStore
      </a>



<a href="https://msdn.microsoft.com/0678e622-3733-499b-b289-c8c181d4638c">ITfPropertyStore</a>
 

 

