---
UID: NF:tuner.IComponentTypes.put_Item
title: IComponentTypes::put_Item (tuner.h)
description: The put_Item method replaces the ComponentType object at the specified index with a new ComponentType object.
helpviewer_keywords: ["IComponentTypes interface [Microsoft TV Technologies]","put_Item method","IComponentTypes.put_Item","IComponentTypes::put_Item","IComponentTypesput_Item","mstv.icomponenttypes_put_item","put_Item","put_Item method [Microsoft TV Technologies]","put_Item method [Microsoft TV Technologies]","IComponentTypes interface","tuner/IComponentTypes::put_Item"]
old-location: mstv\icomponenttypes_put_item.htm
tech.root: mstv
ms.assetid: 1f38e844-d197-40c1-8715-ffe406274b3c
ms.date: 12/05/2018
ms.keywords: IComponentTypes interface [Microsoft TV Technologies],put_Item method, IComponentTypes.put_Item, IComponentTypes::put_Item, IComponentTypesput_Item, mstv.icomponenttypes_put_item, put_Item, put_Item method [Microsoft TV Technologies], put_Item method [Microsoft TV Technologies],IComponentTypes interface, tuner/IComponentTypes::put_Item
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
 - IComponentTypes::put_Item
 - tuner/IComponentTypes::put_Item
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
 - IComponentTypes.put_Item
---

# IComponentTypes::put_Item


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_Item</b> method replaces the <a href="/previous-versions/windows/desktop/legacy/dd693036(v=vs.85)">ComponentType</a> object at the specified index with a new <b>ComponentType</b> object.

## -parameters

### -param Index [in]

Index number of the item to be replaced.

### -param ComponentType [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType</a> object that will be inserted into the collection.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttypes">IComponentTypes Interface</a>