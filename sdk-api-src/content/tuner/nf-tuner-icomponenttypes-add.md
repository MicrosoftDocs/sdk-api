---
UID: NF:tuner.IComponentTypes.Add
title: IComponentTypes::Add (tuner.h)
description: The Add method adds a new ComponentType object to the collection.
helpviewer_keywords: ["Add","Add method [Microsoft TV Technologies]","Add method [Microsoft TV Technologies]","IComponentTypes interface","IComponentTypes interface [Microsoft TV Technologies]","Add method","IComponentTypes.Add","IComponentTypes::Add","IComponentTypesAdd","mstv.icomponenttypes_add","tuner/IComponentTypes::Add"]
old-location: mstv\icomponenttypes_add.htm
tech.root: mstv
ms.assetid: 157f8d81-dbbf-44a7-9786-0758d3c89634
ms.date: 12/05/2018
ms.keywords: Add, Add method [Microsoft TV Technologies], Add method [Microsoft TV Technologies],IComponentTypes interface, IComponentTypes interface [Microsoft TV Technologies],Add method, IComponentTypes.Add, IComponentTypes::Add, IComponentTypesAdd, mstv.icomponenttypes_add, tuner/IComponentTypes::Add
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
 - IComponentTypes::Add
 - tuner/IComponentTypes::Add
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
 - IComponentTypes.Add
---

# IComponentTypes::Add


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Add</b> method adds a new <a href="/previous-versions/windows/desktop/legacy/dd693036(v=vs.85)">ComponentType</a> object to the collection.

## -parameters

### -param ComponentType [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType</a> object that will be added to the collection.

### -param NewIndex [out]

The index number of the component type after it has been added to the collection.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttypes">IComponentTypes Interface</a>