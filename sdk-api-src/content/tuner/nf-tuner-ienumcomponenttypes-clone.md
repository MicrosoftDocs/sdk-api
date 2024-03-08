---
UID: NF:tuner.IEnumComponentTypes.Clone
title: IEnumComponentTypes::Clone (tuner.h)
description: The Clone method creates a new copy of the collection and all its sub-objects.
helpviewer_keywords: ["Clone","Clone method [Microsoft TV Technologies]","Clone method [Microsoft TV Technologies]","IEnumComponentTypes interface","IEnumComponentTypes interface [Microsoft TV Technologies]","Clone method","IEnumComponentTypes.Clone","IEnumComponentTypes::Clone","IEnumComponentTypesClone","mstv.ienumcomponenttypes_clone","tuner/IEnumComponentTypes::Clone"]
old-location: mstv\ienumcomponenttypes_clone.htm
tech.root: mstv
ms.assetid: 777c7302-5b5b-4263-ad9e-3d1bff5328fc
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Microsoft TV Technologies], Clone method [Microsoft TV Technologies],IEnumComponentTypes interface, IEnumComponentTypes interface [Microsoft TV Technologies],Clone method, IEnumComponentTypes.Clone, IEnumComponentTypes::Clone, IEnumComponentTypesClone, mstv.ienumcomponenttypes_clone, tuner/IEnumComponentTypes::Clone
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumComponentTypes::Clone
 - tuner/IEnumComponentTypes::Clone
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IEnumComponentTypes.Clone
---

# IEnumComponentTypes::Clone


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Clone</b> method creates a new copy of the collection and all its sub-objects.

## -parameters

### -param ppEnum [out]

Address of an <b>IEnumComponentTypes</b> interface pointer that will be set to the returned collection object.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ienumcomponenttypes">IEnumComponentTypes Interface</a>