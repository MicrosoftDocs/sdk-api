---
UID: NF:tuner.IComponentTypes.Clone
title: IComponentTypes::Clone (tuner.h)
description: The Clone method creates a new copy of the collection.
helpviewer_keywords: ["Clone","Clone method [Microsoft TV Technologies]","Clone method [Microsoft TV Technologies]","IComponentTypes interface","IComponentTypes interface [Microsoft TV Technologies]","Clone method","IComponentTypes.Clone","IComponentTypes::Clone","IComponentTypesClone","mstv.icomponenttypes_clone","tuner/IComponentTypes::Clone"]
old-location: mstv\icomponenttypes_clone.htm
tech.root: mstv
ms.assetid: 4cc842fa-90bd-4618-8e67-36b15db50cd1
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Microsoft TV Technologies], Clone method [Microsoft TV Technologies],IComponentTypes interface, IComponentTypes interface [Microsoft TV Technologies],Clone method, IComponentTypes.Clone, IComponentTypes::Clone, IComponentTypesClone, mstv.icomponenttypes_clone, tuner/IComponentTypes::Clone
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
 - IComponentTypes::Clone
 - tuner/IComponentTypes::Clone
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
 - IComponentTypes.Clone
---

# IComponentTypes::Clone


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Clone</b> method creates a new copy of the collection.

## -parameters

### -param NewList [out]

Address of an <b>IComponentTypes</b> interface pointer that will be set to the new <a href="/previous-versions/windows/desktop/mstv/componenttypes-object">ComponentTypes</a> object.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttypes">IComponentTypes Interface</a>