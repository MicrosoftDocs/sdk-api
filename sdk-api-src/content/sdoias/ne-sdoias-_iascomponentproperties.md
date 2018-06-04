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

# _IASCOMPONENTPROPERTIES enumeration


## -description


The values of the 
<b>IASCOMPONENTPROPERTIES</b> enumeration type enumerate identifiers for an SDO object.


## -enum-fields




### -field PROPERTY_COMPONENT_ID

The component ID for the SDO object.


### -field PROPERTY_COMPONENT_PROG_ID

The program ID for the SDO object.


### -field PROPERTY_COMPONENT_START

The start value for RADIUS Protocol properties, defined for convenience.


## -remarks



The following code snippet demonstrates obtaining the component ID of an SDO object. The variable pSdo points to an 
<a href="https://msdn.microsoft.com/f8f49bf2-d8cc-40ad-ac52-05d74bcd931c">ISdo</a> interface.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT    hr;
_variant_t    vtProperty;
hr = pSdo-&gt;GetProperty(PROPERTY_COMPONENT_ID, &amp;vtProperty);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f8f49bf2-d8cc-40ad-ac52-05d74bcd931c">ISdo</a>



<a href="https://msdn.microsoft.com/9567e731-4240-4b37-8757-2e25824bba0a">ISdo::GetProperty</a>
 

 

