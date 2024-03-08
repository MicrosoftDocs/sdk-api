---
UID: NF:tuner.IEnumTuningSpaces.Skip
title: IEnumTuningSpaces::Skip (tuner.h)
description: The Skip method skips the specified element in the collection.
helpviewer_keywords: ["IEnumTuningSpaces interface [Microsoft TV Technologies]","Skip method","IEnumTuningSpaces.Skip","IEnumTuningSpaces::Skip","IEnumTuningSpacesSkip","Skip","Skip method [Microsoft TV Technologies]","Skip method [Microsoft TV Technologies]","IEnumTuningSpaces interface","mstv.ienumtuningspaces_skip","tuner/IEnumTuningSpaces::Skip"]
old-location: mstv\ienumtuningspaces_skip.htm
tech.root: mstv
ms.assetid: 5449fca0-4b8d-402e-b444-e7bc314e47b3
ms.date: 12/05/2018
ms.keywords: IEnumTuningSpaces interface [Microsoft TV Technologies],Skip method, IEnumTuningSpaces.Skip, IEnumTuningSpaces::Skip, IEnumTuningSpacesSkip, Skip, Skip method [Microsoft TV Technologies], Skip method [Microsoft TV Technologies],IEnumTuningSpaces interface, mstv.ienumtuningspaces_skip, tuner/IEnumTuningSpaces::Skip
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
 - IEnumTuningSpaces::Skip
 - tuner/IEnumTuningSpaces::Skip
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
 - IEnumTuningSpaces.Skip
---

# IEnumTuningSpaces::Skip


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Skip</b> method skips the specified element in the collection.

## -parameters

### -param celt [in]

The index of the element to skip.

## -returns

Returns S_OK if successful. This method will succeed even if <i>celt</i> is zero. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ienumtuningspaces">IEnumTuningSpaces Interface</a>