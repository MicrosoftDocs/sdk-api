---
UID: NE:sdoias._IASCOMMONPROPERTIES
title: IASCOMMONPROPERTIES (sdoias.h)
description: The values of the IASCOMMONPROPERTIES enumeration type enumerate properties that are present in all SDO objects.
helpviewer_keywords: ["IASCOMMONPROPERTIES","IASCOMMONPROPERTIES enumeration [Network Policy Server]","PROPERTY_SDO_CLASS","PROPERTY_SDO_DATASTORE_NAME","PROPERTY_SDO_DESCRIPTION","PROPERTY_SDO_ID","PROPERTY_SDO_NAME","PROPERTY_SDO_RESERVED","PROPERTY_SDO_START","_sdo_iascommonproperties","nps.SDO_iascommonproperties","sdo.iascommonproperties","sdoias/IASCOMMONPROPERTIES","sdoias/PROPERTY_SDO_CLASS","sdoias/PROPERTY_SDO_DATASTORE_NAME","sdoias/PROPERTY_SDO_DESCRIPTION","sdoias/PROPERTY_SDO_ID","sdoias/PROPERTY_SDO_NAME","sdoias/PROPERTY_SDO_RESERVED","sdoias/PROPERTY_SDO_START"]
old-location: nps\SDO_iascommonproperties.htm
tech.root: Nps
ms.assetid: 9c7ee4d7-987f-45ae-810f-fc310955f36d
ms.date: 12/05/2018
ms.keywords: IASCOMMONPROPERTIES, IASCOMMONPROPERTIES enumeration [Network Policy Server], PROPERTY_SDO_CLASS, PROPERTY_SDO_DATASTORE_NAME, PROPERTY_SDO_DESCRIPTION, PROPERTY_SDO_ID, PROPERTY_SDO_NAME, PROPERTY_SDO_RESERVED, PROPERTY_SDO_START, _sdo_iascommonproperties, nps.SDO_iascommonproperties, sdo.iascommonproperties, sdoias/IASCOMMONPROPERTIES, sdoias/PROPERTY_SDO_CLASS, sdoias/PROPERTY_SDO_DATASTORE_NAME, sdoias/PROPERTY_SDO_DESCRIPTION, sdoias/PROPERTY_SDO_ID, sdoias/PROPERTY_SDO_NAME, sdoias/PROPERTY_SDO_RESERVED, sdoias/PROPERTY_SDO_START
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
targetos: Windows
req.typenames: IASCOMMONPROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IASCOMMONPROPERTIES
 - sdoias/_IASCOMMONPROPERTIES
 - IASCOMMONPROPERTIES
 - sdoias/IASCOMMONPROPERTIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - SdoIas.h
api_name:
 - IASCOMMONPROPERTIES
---

# IASCOMMONPROPERTIES enumeration


## -description

The values of the 
<b>IASCOMMONPROPERTIES</b> enumeration type enumerate properties that are present in all SDO objects.

## -enum-fields

### -field PROPERTY_SDO_RESERVED:0

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

### -field PROPERTY_SDO_START:0x400

Indicates the start of <a href="/windows/desktop/api/sdoias/ne-sdoias-userproperties">USERPROPERTIES</a>.

## -remarks

The following code snippet retrieves the name of the SDO object, if it exists. The variable pSdo is a pointer to an 
<a href="/windows/desktop/api/sdoias/nn-sdoias-isdo">ISdo</a> interface.


```cpp
HRESULT hr;
_variant_t vtItemName;
hr = pSdo->GetProperty(PROPERTY_SDO_NAME, &vtItemName);

```

## -see-also

<a href="/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty">ISdo::GetProperty</a>
