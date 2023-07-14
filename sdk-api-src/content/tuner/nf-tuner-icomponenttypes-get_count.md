---
UID: NF:tuner.IComponentTypes.get_Count
title: IComponentTypes::get_Count (tuner.h)
description: The get_Count method returns the number of component types in the collection.
helpviewer_keywords: ["IComponentTypes interface [Microsoft TV Technologies]","get_Count method","IComponentTypes.get_Count","IComponentTypes::get_Count","IComponentTypesget_Count","get_Count","get_Count method [Microsoft TV Technologies]","get_Count method [Microsoft TV Technologies]","IComponentTypes interface","mstv.icomponenttypes_get_count","tuner/IComponentTypes::get_Count"]
old-location: mstv\icomponenttypes_get_count.htm
tech.root: mstv
ms.assetid: 9f353702-1be1-4fa0-9312-f76f23f63a2b
ms.date: 12/05/2018
ms.keywords: IComponentTypes interface [Microsoft TV Technologies],get_Count method, IComponentTypes.get_Count, IComponentTypes::get_Count, IComponentTypesget_Count, get_Count, get_Count method [Microsoft TV Technologies], get_Count method [Microsoft TV Technologies],IComponentTypes interface, mstv.icomponenttypes_get_count, tuner/IComponentTypes::get_Count
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
 - IComponentTypes::get_Count
 - tuner/IComponentTypes::get_Count
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
 - IComponentTypes.get_Count
---

# IComponentTypes::get_Count


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Count</b> method returns the number of component types in the collection.

## -parameters

### -param Count [out]

Receives the number of items in the collection.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttypes">IComponentTypes Interface</a>