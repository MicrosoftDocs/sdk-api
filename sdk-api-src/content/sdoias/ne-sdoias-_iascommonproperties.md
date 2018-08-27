---
UID: NE:sdoias._IASCOMMONPROPERTIES
title: "_IASCOMMONPROPERTIES"
author: windows-sdk-content
description: The values of the IASCOMMONPROPERTIES enumeration type enumerate properties that are present in all SDO objects.
old-location: nps\SDO_iascommonproperties.htm
old-project: nps
ms.assetid: 9c7ee4d7-987f-45ae-810f-fc310955f36d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IASCOMMONPROPERTIES, IASCOMMONPROPERTIES enumeration [Network Policy Server], PROPERTY_SDO_CLASS, PROPERTY_SDO_DATASTORE_NAME, PROPERTY_SDO_DESCRIPTION, PROPERTY_SDO_ID, PROPERTY_SDO_NAME, PROPERTY_SDO_RESERVED, PROPERTY_SDO_START, _IASCOMMONPROPERTIES, _sdo_iascommonproperties, nps.SDO_iascommonproperties, sdo.iascommonproperties, sdoias/IASCOMMONPROPERTIES, sdoias/PROPERTY_SDO_CLASS, sdoias/PROPERTY_SDO_DATASTORE_NAME, sdoias/PROPERTY_SDO_DESCRIPTION, sdoias/PROPERTY_SDO_ID, sdoias/PROPERTY_SDO_NAME, sdoias/PROPERTY_SDO_RESERVED, sdoias/PROPERTY_SDO_START
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: sdoias.h
req.include-header: 
req.redist: 
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
req.product: ADAM
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

Indicates the start of <a href="https://msdn.microsoft.com/ce16b0e4-3be1-42fc-a489-d3ddce2ebf3f">USERPROPERTIES</a>.


## -remarks



The following code snippet retrieves the name of the SDO object, if it exists. The variable pSdo is a pointer to an 
<a href="https://msdn.microsoft.com/f8f49bf2-d8cc-40ad-ac52-05d74bcd931c">ISdo</a> interface.


```cpp
HRESULT hr;
_variant_t vtItemName;
hr = pSdo->GetProperty(PROPERTY_SDO_NAME, &vtItemName);

```





## -see-also




<a href="https://msdn.microsoft.com/9567e731-4240-4b37-8757-2e25824bba0a">ISdo::GetProperty</a>
 

 

