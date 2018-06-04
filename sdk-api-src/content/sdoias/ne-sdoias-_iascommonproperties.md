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

# _IASCOMMONPROPERTIES enumeration


## -description


The values of the 
<b>IASCOMMONPROPERTIES</b> enumeration type enumerate properties that are present in all SDO objects.


## -enum-fields




### -field PROPERTY_SDO_RESERVED

This property is reserved.


### -field PROPERTY_SDO_CLASS

The program ID for the SDO object.


### -field PROPERTY_SDO_NAME

The name of the SDO object.


### -field PROPERTY_SDO_DESCRIPTION

Reserved for future use.


### -field PROPERTY_SDO_ID

Reserved for future use.


### -field PROPERTY_SDO_DATASTORE_NAME

The name of the datastore for the object.


### -field PROPERTY_SDO_TEMPLATE_GUID


### -field PROPERTY_SDO_OPAQUE


### -field PROPERTY_SDO_START

Indicates the start of <a href="https://msdn.microsoft.com/library/windows/hardware/hh973206">USERPROPERTIES</a>.


## -remarks



The following code snippet retrieves the name of the SDO object, if it exists. The variable pSdo is a pointer to an 
<a href="https://msdn.microsoft.com/f8f49bf2-d8cc-40ad-ac52-05d74bcd931c">ISdo</a> interface.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT hr;
_variant_t vtItemName;
hr = pSdo-&gt;GetProperty(PROPERTY_SDO_NAME, &amp;vtItemName);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/9567e731-4240-4b37-8757-2e25824bba0a">ISdo::GetProperty</a>
 

 

