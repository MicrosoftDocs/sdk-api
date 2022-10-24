---
UID: NN:propidl.IEnumSTATPROPSTG
title: IEnumSTATPROPSTG (propidl.h)
description: The IEnumSTATPROPSTG interface iterates through an array of STATPROPSTG structures. The STATPROPSTG structures contain statistical data about properties in a property set. 
helpviewer_keywords: ["IEnumSTATPROPSTG","IEnumSTATPROPSTG interface [Structured Storage]","IEnumSTATPROPSTG interface [Structured Storage]","described","_stg_ienumstatpropstg","propidlbase/IEnumSTATPROPSTG","stg.ienumstatpropstg"]
old-location: stg\ienumstatpropstg.htm
tech.root: Stg
ms.assetid: e625e52a-5628-4d18-9282-aa1c141c83af
ms.date: 08/02/2022
ms.keywords: IEnumSTATPROPSTG, IEnumSTATPROPSTG interface [Structured Storage], IEnumSTATPROPSTG interface [Structured Storage],described, _stg_ienumstatpropstg, propidlbase/IEnumSTATPROPSTG, stg.ienumstatpropstg
req.header: propidl.h
req.include-header: Propidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumSTATPROPSTG
 - propidl/IEnumSTATPROPSTG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IEnumSTATPROPSTG
---

# IEnumSTATPROPSTG interface


## -description

The 
<b>IEnumSTATPROPSTG</b> interface iterates through an array of 
<a href="/windows/desktop/api/propidl/ns-propidl-statpropstg">STATPROPSTG</a> structures. The <b>STATPROPSTG</b> structures contain statistical data about properties in a property set. <b>IEnumSTATPROPSTG</b> has the same methods as all enumerator interfaces: <a href="/windows/desktop/api/propidl/nf-propidl-ienumstatpropstg-next">Next</a>, <a href="/windows/desktop/api/propidl/nf-propidl-ienumstatpropstg-skip">Skip</a>, <a href="/windows/desktop/api/propidl/nf-propidl-ienumstatpropstg-reset">Reset</a>, and 
<a href="/windows/desktop/api/propidl/nf-propidl-ienumstatpropstg-clone">Clone</a>.

The implementation defines the order in which the properties in the set are enumerated. Properties that are present when the enumerator is created, and are not removed during the enumeration, will be enumerated only once. Properties added or deleted while the enumeration is in progress may or may not be enumerated, but will never be enumerated more than once.


<a href="/windows/desktop/Stg/reserved-property-identifiers">Reserved property identifiers</a>, properties with a property ID of 0 (dictionary), 1 (code page indicator), or greater than or equal to 0x80000000 are not enumerated.

Enumeration of a nonsimple property does not necessarily indicate that the property can be read successfully through a call to <a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-readmultiple">IPropertyStorage::ReadMultiple</a>. This is because the performance overhead of checking existence of the indirect stream or storage is prohibitive during property enumeration.

## -inheritance

The <b>IEnumSTATPROPSTG</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumSTATPROPSTG</b> also has these types of members:

## -see-also

<a href="/windows/desktop/Stg/enumall-sample">EnumAll Sample</a>



<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-enum">IPropertyStorage::Enum</a>
