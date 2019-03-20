---
UID: NE:sdoias._IASCOMPONENTPROPERTIES
title: IASCOMPONENTPROPERTIES (sdoias.h)
author: windows-sdk-content
description: The values of the IASCOMPONENTPROPERTIES enumeration type enumerate identifiers for an SDO object.
old-location: nps\SDO_iascomponentproperties.htm
tech.root: Nps
ms.assetid: 5b2ab351-88b8-4a9d-9954-883d9e251b4c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IASCOMPONENTPROPERTIES, IASCOMPONENTPROPERTIES enumeration [Network Policy Server], PROPERTY_COMPONENT_ID, PROPERTY_COMPONENT_PROG_ID, PROPERTY_COMPONENT_START, _sdo_iascomponentproperties, nps.SDO_iascomponentproperties, sdo.iascomponentproperties, sdoias/IASCOMPONENTPROPERTIES, sdoias/PROPERTY_COMPONENT_ID, sdoias/PROPERTY_COMPONENT_PROG_ID, sdoias/PROPERTY_COMPONENT_START
ms.topic: enum
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SdoIas.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - SdoIas.h
api_name:
 - IASCOMPONENTPROPERTIES
product: Windows
targetos: Windows
req.typenames: IASCOMPONENTPROPERTIES
req.redist: 
---

# IASCOMPONENTPROPERTIES enumeration


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


```cpp
HRESULT    hr;
_variant_t    vtProperty;
hr = pSdo->GetProperty(PROPERTY_COMPONENT_ID, &vtProperty);

```





## -see-also




<a href="https://msdn.microsoft.com/f8f49bf2-d8cc-40ad-ac52-05d74bcd931c">ISdo</a>



<a href="https://msdn.microsoft.com/9567e731-4240-4b37-8757-2e25824bba0a">ISdo::GetProperty</a>
 

 

