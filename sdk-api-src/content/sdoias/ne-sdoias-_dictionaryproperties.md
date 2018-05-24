---
UID: NE:sdoias._DICTIONARYPROPERTIES
title: "_DICTIONARYPROPERTIES"
author: windows-driver-content
description: The values of the DICTIONARYPROPERTIES properties type enumerate properties associated with the attribute dictionary.
old-location: nps\SDO_dictionaryproperties.htm
old-project: Nps
ms.assetid: 47da09d8-9b45-4910-a6b1-1759c5000482
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: DICTIONARYPROPERTIES, DICTIONARYPROPERTIES enumeration [Network Policy Server], PROPERTY_DICTIONARY_ATTRIBUTES_COLLECTION, PROPERTY_DICTIONARY_LOCATION, _DICTIONARYPROPERTIES, _sdo_dictionaryproperties, nps.SDO_dictionaryproperties, sdo.dictionaryproperties, sdoias/DICTIONARYPROPERTIES, sdoias/PROPERTY_DICTIONARY_ATTRIBUTES_COLLECTION, sdoias/PROPERTY_DICTIONARY_LOCATION
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DICTIONARYPROPERTIES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	SdoIas.h
api_name:
-	DICTIONARYPROPERTIES
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _DICTIONARYPROPERTIES enumeration


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




<a href="https://msdn.microsoft.com/eb8cff95-4ea3-446c-893f-3065d3a037d3">ATTRIBUTEPROPERTIES</a>



<a href="https://msdn.microsoft.com/f8f49bf2-d8cc-40ad-ac52-05d74bcd931c">ISdo</a>



<a href="https://msdn.microsoft.com/172444be-b2a2-4060-af92-b0c63f0ffe6b">ISdoMachine::GetDictionarySDO</a>
 

 

