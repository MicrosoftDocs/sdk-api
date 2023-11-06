---
UID: NF:tuner.IComponentTypes.EnumComponentTypes
title: IComponentTypes::EnumComponentTypes (tuner.h)
description: The EnumComponentTypes method returns an IEnumComponentTypes enumerator for all component types in the collection.
helpviewer_keywords: ["EnumComponentTypes","EnumComponentTypes method [Microsoft TV Technologies]","EnumComponentTypes method [Microsoft TV Technologies]","IComponentTypes interface","IComponentTypes interface [Microsoft TV Technologies]","EnumComponentTypes method","IComponentTypes.EnumComponentTypes","IComponentTypes::EnumComponentTypes","IComponentTypesEnumComponentTypes","mstv.icomponenttypes_enumcomponenttypes","tuner/IComponentTypes::EnumComponentTypes"]
old-location: mstv\icomponenttypes_enumcomponenttypes.htm
tech.root: mstv
ms.assetid: c070998c-4350-4630-80c0-e3db46154845
ms.date: 12/05/2018
ms.keywords: EnumComponentTypes, EnumComponentTypes method [Microsoft TV Technologies], EnumComponentTypes method [Microsoft TV Technologies],IComponentTypes interface, IComponentTypes interface [Microsoft TV Technologies],EnumComponentTypes method, IComponentTypes.EnumComponentTypes, IComponentTypes::EnumComponentTypes, IComponentTypesEnumComponentTypes, mstv.icomponenttypes_enumcomponenttypes, tuner/IComponentTypes::EnumComponentTypes
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
 - IComponentTypes::EnumComponentTypes
 - tuner/IComponentTypes::EnumComponentTypes
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
 - IComponentTypes.EnumComponentTypes
---

# IComponentTypes::EnumComponentTypes


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>EnumComponentTypes</b> method returns an <b>IEnumComponentTypes</b> enumerator for all component types in the collection.

## -parameters

### -param ppNewEnum [out]

Receives a pointer to the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ienumcomponenttypes">IEnumComponentTypes</a> interface. The caller must release the interface.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttypes">IComponentTypes Interface</a>