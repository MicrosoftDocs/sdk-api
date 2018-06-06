---
UID: NE:sdoias._IASCOMMONPROPERTIES
title: "_IASCOMMONPROPERTIES"
author: windows-sdk-content
description: The values of the IASCOMMONPROPERTIES enumeration type enumerate properties that are present in all SDO objects.
old-location: nps\SDO_iascommonproperties.htm
old-project: Nps
ms.assetid: 9c7ee4d7-987f-45ae-810f-fc310955f36d
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IASCOMMONPROPERTIES, IASCOMMONPROPERTIES enumeration [Network Policy Server], PROPERTY_SDO_CLASS, PROPERTY_SDO_DATASTORE_NAME, PROPERTY_SDO_DESCRIPTION, PROPERTY_SDO_ID, PROPERTY_SDO_NAME, PROPERTY_SDO_RESERVED, PROPERTY_SDO_START, _IASCOMMONPROPERTIES, _sdo_iascommonproperties, nps.SDO_iascommonproperties, sdo.iascommonproperties, sdoias/IASCOMMONPROPERTIES, sdoias/PROPERTY_SDO_CLASS, sdoias/PROPERTY_SDO_DATASTORE_NAME, sdoias/PROPERTY_SDO_DESCRIPTION, sdoias/PROPERTY_SDO_ID, sdoias/PROPERTY_SDO_NAME, sdoias/PROPERTY_SDO_RESERVED, sdoias/PROPERTY_SDO_START
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ConvertStringSidToSidW (Unicode) and ConvertStringSidToSidA (ANSI)
req.idl: SdoIas.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: IASCOMMONPROPERTIES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - SdoIas.h
api_name:
 - IASCOMMONPROPERTIES
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

