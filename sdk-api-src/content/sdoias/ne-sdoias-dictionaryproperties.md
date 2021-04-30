---
UID: NE:sdoias._DICTIONARYPROPERTIES
title: DICTIONARYPROPERTIES (sdoias.h)
description: The values of the DICTIONARYPROPERTIES properties type enumerate properties associated with the attribute dictionary.
helpviewer_keywords: ["DICTIONARYPROPERTIES","DICTIONARYPROPERTIES enumeration [Network Policy Server]","PROPERTY_DICTIONARY_ATTRIBUTES_COLLECTION","PROPERTY_DICTIONARY_LOCATION","_sdo_dictionaryproperties","nps.SDO_dictionaryproperties","sdo.dictionaryproperties","sdoias/DICTIONARYPROPERTIES","sdoias/PROPERTY_DICTIONARY_ATTRIBUTES_COLLECTION","sdoias/PROPERTY_DICTIONARY_LOCATION"]
old-location: nps\SDO_dictionaryproperties.htm
tech.root: Nps
ms.assetid: 47da09d8-9b45-4910-a6b1-1759c5000482
ms.date: 12/05/2018
ms.keywords: DICTIONARYPROPERTIES, DICTIONARYPROPERTIES enumeration [Network Policy Server], PROPERTY_DICTIONARY_ATTRIBUTES_COLLECTION, PROPERTY_DICTIONARY_LOCATION, _sdo_dictionaryproperties, nps.SDO_dictionaryproperties, sdo.dictionaryproperties, sdoias/DICTIONARYPROPERTIES, sdoias/PROPERTY_DICTIONARY_ATTRIBUTES_COLLECTION, sdoias/PROPERTY_DICTIONARY_LOCATION
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
req.typenames: DICTIONARYPROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DICTIONARYPROPERTIES
 - sdoias/_DICTIONARYPROPERTIES
 - DICTIONARYPROPERTIES
 - sdoias/DICTIONARYPROPERTIES
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
 - DICTIONARYPROPERTIES
---

# DICTIONARYPROPERTIES enumeration


## -description

The values of the 
<b>DICTIONARYPROPERTIES</b> properties type enumerate properties associated with the attribute dictionary.

## -enum-fields

### -field PROPERTY_DICTIONARY_ATTRIBUTES_COLLECTION

The collection of all possible attributes.

### -field PROPERTY_DICTIONARY_LOCATION

The location of the datastore that contains the dictionary. This property is read-only.

## -remarks

The dictionary is the collection of all possible attributes. It includes some attributes that are reserved for system use.

## -see-also

<a href="/windows/desktop/api/sdoias/ne-sdoias-attributeproperties">ATTRIBUTEPROPERTIES</a>



<a href="/windows/desktop/api/sdoias/nn-sdoias-isdo">ISdo</a>



<a href="/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getdictionarysdo">ISdoMachine::GetDictionarySDO</a>