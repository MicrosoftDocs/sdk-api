---
UID: NN:propidlbase.IEnumSTATPROPSETSTG
title: IEnumSTATPROPSETSTG (propidlbase.h)
description: The IEnumSTATPROPSETSTG interface iterates through an array of STATPROPSETSTG structures containing statistical data about the property sets managed by the current IPropertySetStorage instance. 
helpviewer_keywords: ["IEnumSTATPROPSETSTG","IEnumSTATPROPSETSTG interface [Structured Storage]","IEnumSTATPROPSETSTG interface [Structured Storage]","described","_stg_ienumstatpropsetstg","propidlbase/IEnumSTATPROPSETSTG","stg.ienumstatpropsetstg"]
old-location: stg\ienumstatpropsetstg.htm
tech.root: Stg
ms.assetid: 8d5e658f-312c-4c91-8794-808b2e8dd182
ms.date: 08/02/2022
ms.keywords: IEnumSTATPROPSETSTG, IEnumSTATPROPSETSTG interface [Structured Storage], IEnumSTATPROPSETSTG interface [Structured Storage],described, _stg_ienumstatpropsetstg, propidlbase/IEnumSTATPROPSETSTG, stg.ienumstatpropsetstg
req.header: propidlbase.h
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
 - IEnumSTATPROPSETSTG
 - propidlbase/IEnumSTATPROPSETSTG
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
 - IEnumSTATPROPSETSTG
---

# IEnumSTATPROPSETSTG interface


## -description

The 
<b>IEnumSTATPROPSETSTG</b> interface iterates through an array of 
<a href="/windows/desktop/api/propidl/ns-propidl-statpropsetstg">STATPROPSETSTG</a> structures. The <b>STATPROPSETSTG</b> structures contain statistical data about the property sets managed by the current <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a> instance. <b>IEnumSTATPROPSETSTG</b> has the same methods as all enumerator interfaces: <a href="/windows/desktop/api/propidl/nf-propidl-ienumstatpropsetstg-next">Next</a>, <a href="/windows/desktop/api/propidl/nf-propidl-ienumstatpropsetstg-skip">Skip</a>, <a href="/windows/desktop/api/propidl/nf-propidl-ienumstatpropsetstg-reset">Reset</a>, and 
<a href="/windows/desktop/api/propidl/nf-propidl-ienumstatpropsetstg-clone">Clone</a>.

The implementation defines the order in which the property sets are enumerated. Property sets that are present when the enumerator is created, and are not removed during the enumeration, will be enumerated only once. Property sets added or deleted while the enumeration is in progress may or may not be enumerated, but, if enumerated, will not be enumerated more than once.

For more information about how the COM compound document implementation of <a href="/windows/desktop/api/propidl/nf-propidl-ienumstatpropsetstg-next">IEnumSTATPROPSETSTG::Next</a> supplies members of the 
<a href="/windows/desktop/api/propidl/ns-propidl-statpropsetstg">STATPROPSETSTG</a> structure, see <a href="/windows/desktop/Stg/ienumstatpropsetstg-compound-file-implementation">IEnumSTATPROPSETSTG--Compound File Implementation</a>.

## -inheritance

The <b>IEnumSTATPROPSETSTG</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumSTATPROPSETSTG</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-enum">IPropertyStorage::Enum</a>
