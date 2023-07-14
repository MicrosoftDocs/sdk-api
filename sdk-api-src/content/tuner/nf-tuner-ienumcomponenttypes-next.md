---
UID: NF:tuner.IEnumComponentTypes.Next
title: IEnumComponentTypes::Next (tuner.h)
description: The Next method retrieves the next n elements in the collection.
helpviewer_keywords: ["IEnumComponentTypes interface [Microsoft TV Technologies]","Next method","IEnumComponentTypes.Next","IEnumComponentTypes::Next","IEnumComponentTypesNext","Next","Next method [Microsoft TV Technologies]","Next method [Microsoft TV Technologies]","IEnumComponentTypes interface","mstv.ienumcomponenttypes_next","tuner/IEnumComponentTypes::Next"]
old-location: mstv\ienumcomponenttypes_next.htm
tech.root: mstv
ms.assetid: 491e9237-38cd-4c12-b93b-eb398a49d742
ms.date: 12/05/2018
ms.keywords: IEnumComponentTypes interface [Microsoft TV Technologies],Next method, IEnumComponentTypes.Next, IEnumComponentTypes::Next, IEnumComponentTypesNext, Next, Next method [Microsoft TV Technologies], Next method [Microsoft TV Technologies],IEnumComponentTypes interface, mstv.ienumcomponenttypes_next, tuner/IEnumComponentTypes::Next
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
 - IEnumComponentTypes::Next
 - tuner/IEnumComponentTypes::Next
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
 - IEnumComponentTypes.Next
---

# IEnumComponentTypes::Next


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Next</b> method retrieves the next <i>n</i> elements in the collection.

## -parameters

### -param celt [in]

The number of elements to retrieve.

### -param rgelt [out]

Address of an array of <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType</a> interface pointers that will receive the returned <a href="/previous-versions/windows/desktop/legacy/dd693036(v=vs.85)">ComponentType</a> objects.

### -param pceltFetched [out]

Receives the number of elements actually retrieved.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ienumcomponenttypes">IEnumComponentTypes Interface</a>