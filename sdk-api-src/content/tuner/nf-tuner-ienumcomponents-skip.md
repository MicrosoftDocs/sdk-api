---
UID: NF:tuner.IEnumComponents.Skip
title: IEnumComponents::Skip (tuner.h)
description: The Skip method skips the specified element in the collection without retrieving it.
helpviewer_keywords: ["IEnumComponents interface [Microsoft TV Technologies]","Skip method","IEnumComponents.Skip","IEnumComponents::Skip","IEnumComponentsSkip","Skip","Skip method [Microsoft TV Technologies]","Skip method [Microsoft TV Technologies]","IEnumComponents interface","mstv.ienumcomponents_skip","tuner/IEnumComponents::Skip"]
old-location: mstv\ienumcomponents_skip.htm
tech.root: mstv
ms.assetid: f63eca00-c47c-4b9f-8f7a-7080c23653ce
ms.date: 12/05/2018
ms.keywords: IEnumComponents interface [Microsoft TV Technologies],Skip method, IEnumComponents.Skip, IEnumComponents::Skip, IEnumComponentsSkip, Skip, Skip method [Microsoft TV Technologies], Skip method [Microsoft TV Technologies],IEnumComponents interface, mstv.ienumcomponents_skip, tuner/IEnumComponents::Skip
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
 - IEnumComponents::Skip
 - tuner/IEnumComponents::Skip
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
 - IEnumComponents.Skip
---

# IEnumComponents::Skip


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Skip</b> method skips the specified element in the collection without retrieving it.

## -parameters

### -param celt [in]

Specifies the element to skip.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ienumcomponents">IEnumComponents Interface</a>