---
UID: NF:tuner.IEnumComponentTypes.Skip
title: IEnumComponentTypes::Skip (tuner.h)
description: The Skip method skips the element at the specified index.
helpviewer_keywords: ["IEnumComponentTypes interface [Microsoft TV Technologies]","Skip method","IEnumComponentTypes.Skip","IEnumComponentTypes::Skip","IEnumComponentTypesSkip","Skip","Skip method [Microsoft TV Technologies]","Skip method [Microsoft TV Technologies]","IEnumComponentTypes interface","mstv.ienumcomponenttypes_skip","tuner/IEnumComponentTypes::Skip"]
old-location: mstv\ienumcomponenttypes_skip.htm
tech.root: mstv
ms.assetid: ea6c0ff8-76ae-4783-9b99-154ecb210a17
ms.date: 12/05/2018
ms.keywords: IEnumComponentTypes interface [Microsoft TV Technologies],Skip method, IEnumComponentTypes.Skip, IEnumComponentTypes::Skip, IEnumComponentTypesSkip, Skip, Skip method [Microsoft TV Technologies], Skip method [Microsoft TV Technologies],IEnumComponentTypes interface, mstv.ienumcomponenttypes_skip, tuner/IEnumComponentTypes::Skip
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
 - IEnumComponentTypes::Skip
 - tuner/IEnumComponentTypes::Skip
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
 - IEnumComponentTypes.Skip
---

# IEnumComponentTypes::Skip


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Skip</b> method skips the element at the specified index.

## -parameters

### -param celt [in]

Index of the element to skip.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ienumcomponenttypes">IEnumComponentTypes Interface</a>