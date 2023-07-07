---
UID: NF:tuner.IComponents.get_Item
title: IComponents::get_Item (tuner.h)
description: The get_Item method enables the caller to access a component by index.
helpviewer_keywords: ["IComponents interface [Microsoft TV Technologies]","get_Item method","IComponents.get_Item","IComponents::get_Item","IComponentsget_Item","get_Item","get_Item method [Microsoft TV Technologies]","get_Item method [Microsoft TV Technologies]","IComponents interface","mstv.icomponents_get_item","tuner/IComponents::get_Item"]
old-location: mstv\icomponents_get_item.htm
tech.root: mstv
ms.assetid: 12716c7c-3156-401e-8f1c-be3100afb912
ms.date: 12/05/2018
ms.keywords: IComponents interface [Microsoft TV Technologies],get_Item method, IComponents.get_Item, IComponents::get_Item, IComponentsget_Item, get_Item, get_Item method [Microsoft TV Technologies], get_Item method [Microsoft TV Technologies],IComponents interface, mstv.icomponents_get_item, tuner/IComponents::get_Item
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
 - IComponents::get_Item
 - tuner/IComponents::get_Item
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
 - IComponents.get_Item
---

# IComponents::get_Item


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Item</b> method enables the caller to access a component by index.

## -parameters

### -param Index [in]

Variable of type <b>VARIANT</b> specifying the zero-based index in the collection.

### -param ppComponent [out]

Address of an <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponent">IComponent</a> interface pointer that will receive the <b>Component</b> object at the specified index.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponents">IComponents Interface</a>