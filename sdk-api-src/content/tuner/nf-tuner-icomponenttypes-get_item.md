---
UID: NF:tuner.IComponentTypes.get_Item
title: IComponentTypes::get_Item (tuner.h)
description: The get_Item method retrieves the IComponentType interface pointer at the specified index number.
helpviewer_keywords: ["IComponentTypes interface [Microsoft TV Technologies]","get_Item method","IComponentTypes.get_Item","IComponentTypes::get_Item","IComponentTypesget_Item","get_Item","get_Item method [Microsoft TV Technologies]","get_Item method [Microsoft TV Technologies]","IComponentTypes interface","mstv.icomponenttypes_get_item","tuner/IComponentTypes::get_Item"]
old-location: mstv\icomponenttypes_get_item.htm
tech.root: mstv
ms.assetid: be2e6f1b-a9af-4c19-ae25-a096ceee96fc
ms.date: 12/05/2018
ms.keywords: IComponentTypes interface [Microsoft TV Technologies],get_Item method, IComponentTypes.get_Item, IComponentTypes::get_Item, IComponentTypesget_Item, get_Item, get_Item method [Microsoft TV Technologies], get_Item method [Microsoft TV Technologies],IComponentTypes interface, mstv.icomponenttypes_get_item, tuner/IComponentTypes::get_Item
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
 - IComponentTypes::get_Item
 - tuner/IComponentTypes::get_Item
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
 - IComponentTypes.get_Item
---

# IComponentTypes::get_Item


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Item</b> method retrieves the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType</a> interface pointer at the specified index number.

## -parameters

### -param Index [in]

The index number of the object to retrieve.

### -param ComponentType [out]

Receives a pointer to the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType</a> interface. The caller must release the interface.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttypes">IComponentTypes Interface</a>