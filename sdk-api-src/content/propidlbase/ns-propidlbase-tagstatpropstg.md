---
UID: NS:propidlbase.tagSTATPROPSTG
title: tagSTATPROPSTG
author: windows-driver-content
description: Contains data about a single property in a property set. This data is the property ID and type tag, and the optional string name that may be associated with the property.
old-location: stg\statpropstg.htm
old-project: Stg
ms.assetid: 3b8de6d3-18a3-4c0a-94d1-04bcec05d41a
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: STATPROPSTG, STATPROPSTG [Strctd Stg], STATPROPSTG structure [Structured Storage], _stg_statpropstg, propidlbase/STATPROPSTG, stg.statpropstg, tagSTATPROPSTG
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: propidlbase.h
req.include-header: Propidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: STATPROPSTG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	propidlbase.h
api_name:
-	STATPROPSTG
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# tagSTATPROPSTG structure


## -description



			The 
<b>STATPROPSTG</b> structure contains data about a single property in a property set. This data is the property ID and type tag, and the optional string name that may be associated with the property.


<a href="https://msdn.microsoft.com/73f834cf-b6e4-4a48-bbdc-0c4ba87aacaf">IPropertyStorage::Enum</a> supplies a pointer to the 
<a href="https://msdn.microsoft.com/e625e52a-5628-4d18-9282-aa1c141c83af">IEnumSTATPROPSTG</a> interface on an enumerator object that can be used to enumerate the 
<b>STATPROPSTG</b> structures for the properties in the current property set. 
<b>STATPROPSTG</b> is defined as:


## -struct-fields




### -field lpwstrName

A wide-character null-terminated Unicode string that contains the optional string name associated with the property. May be <b>NULL</b>. This member must be freed using 
<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a>.


### -field propid

A 32-bit identifier that uniquely identifies the property within the property set. All properties within property sets must have unique property identifiers.


### -field vt

The property type.


## -see-also




<a href="https://msdn.microsoft.com/e625e52a-5628-4d18-9282-aa1c141c83af">IEnumSTATPROPSTG</a>



<a href="https://msdn.microsoft.com/73f834cf-b6e4-4a48-bbdc-0c4ba87aacaf">IPropertyStorage::Enum</a>
 

 

