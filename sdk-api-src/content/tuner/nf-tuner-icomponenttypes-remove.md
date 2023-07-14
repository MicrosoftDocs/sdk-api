---
UID: NF:tuner.IComponentTypes.Remove
title: IComponentTypes::Remove (tuner.h)
description: The Remove method removes the ComponentType object at the specified index number.
helpviewer_keywords: ["IComponentTypes interface [Microsoft TV Technologies]","Remove method","IComponentTypes.Remove","IComponentTypes::Remove","IComponentTypesRemove","Remove","Remove method [Microsoft TV Technologies]","Remove method [Microsoft TV Technologies]","IComponentTypes interface","mstv.icomponenttypes_remove","tuner/IComponentTypes::Remove"]
old-location: mstv\icomponenttypes_remove.htm
tech.root: mstv
ms.assetid: 7344851a-51ba-41c0-b368-e5eecfb5fb08
ms.date: 12/05/2018
ms.keywords: IComponentTypes interface [Microsoft TV Technologies],Remove method, IComponentTypes.Remove, IComponentTypes::Remove, IComponentTypesRemove, Remove, Remove method [Microsoft TV Technologies], Remove method [Microsoft TV Technologies],IComponentTypes interface, mstv.icomponenttypes_remove, tuner/IComponentTypes::Remove
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
 - IComponentTypes::Remove
 - tuner/IComponentTypes::Remove
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
 - IComponentTypes.Remove
---

# IComponentTypes::Remove


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Remove</b> method removes the <a href="/previous-versions/windows/desktop/legacy/dd693036(v=vs.85)">ComponentType</a> object at the specified index number.

## -parameters

### -param Index [in]

Index of the item to remove.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttypes">IComponentTypes Interface</a>