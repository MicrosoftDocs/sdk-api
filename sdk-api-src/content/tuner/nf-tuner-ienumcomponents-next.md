---
UID: NF:tuner.IEnumComponents.Next
title: IEnumComponents::Next (tuner.h)
description: The Next method retrieves the next n elements in the collection.
helpviewer_keywords: ["IEnumComponents interface [Microsoft TV Technologies]","Next method","IEnumComponents.Next","IEnumComponents::Next","IEnumComponentsNext","Next","Next method [Microsoft TV Technologies]","Next method [Microsoft TV Technologies]","IEnumComponents interface","mstv.ienumcomponents_next","tuner/IEnumComponents::Next"]
old-location: mstv\ienumcomponents_next.htm
tech.root: mstv
ms.assetid: 73cb45c7-1f74-46cf-a410-ec1d5fed4271
ms.date: 12/05/2018
ms.keywords: IEnumComponents interface [Microsoft TV Technologies],Next method, IEnumComponents.Next, IEnumComponents::Next, IEnumComponentsNext, Next, Next method [Microsoft TV Technologies], Next method [Microsoft TV Technologies],IEnumComponents interface, mstv.ienumcomponents_next, tuner/IEnumComponents::Next
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
 - IEnumComponents::Next
 - tuner/IEnumComponents::Next
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
 - IEnumComponents.Next
---

# IEnumComponents::Next


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Next</b> method retrieves the next <i>n</i> elements in the collection.

## -parameters

### -param celt [in]

The number of elements to retrieve.

### -param rgelt [out]

Address of an array of <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponent">IComponent</a> interface pointers that will receive the retrieved <a href="/previous-versions/windows/desktop/mstv/component-object">Component</a> objects.

### -param pceltFetched [out]

Receives the number of elements actually retrieved.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ienumcomponents">IEnumComponents Interface</a>