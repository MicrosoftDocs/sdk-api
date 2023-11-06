---
UID: NF:tuner.IComponents.put_Item
title: IComponents::put_Item (tuner.h)
description: The put_Item method inserts a component into the collection, replacing the item that is identified by the specified index.
helpviewer_keywords: ["IComponents interface [Microsoft TV Technologies]","put_Item method","IComponents.put_Item","IComponents::put_Item","IComponentsput_Item","mstv.icomponents_put_item","put_Item","put_Item method [Microsoft TV Technologies]","put_Item method [Microsoft TV Technologies]","IComponents interface","tuner/IComponents::put_Item"]
old-location: mstv\icomponents_put_item.htm
tech.root: mstv
ms.assetid: c1e18e97-e8d3-441c-b7ea-6743e478033b
ms.date: 12/05/2018
ms.keywords: IComponents interface [Microsoft TV Technologies],put_Item method, IComponents.put_Item, IComponents::put_Item, IComponentsput_Item, mstv.icomponents_put_item, put_Item, put_Item method [Microsoft TV Technologies], put_Item method [Microsoft TV Technologies],IComponents interface, tuner/IComponents::put_Item
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
 - IComponents::put_Item
 - tuner/IComponents::put_Item
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
 - IComponents.put_Item
---

# IComponents::put_Item


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_Item</b> method inserts a component into the collection, replacing the item that is identified by the specified index.

## -parameters

### -param Index [in]

Specifies the index to assign to the component. This parameter is a value of type <b>VARIANT</b>.

### -param ppComponent [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponent">IComponent</a> interface of the component object. The method creates a clone of the component and inserts the clone into the collection.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

This method allows the client to replace an existing item in the collection.

If the collection contains <i>n</i> items, valid indexes are in the range 0 to <i>n</i>-1. To determine the number of items in the collection, call <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponents-get_count">get_Count</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponents">IComponents Interface</a>



<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponents-get_item">get_Item</a>