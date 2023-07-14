---
UID: NF:tuner.IEnumTuningSpaces.Next
title: IEnumTuningSpaces::Next (tuner.h)
description: The Next method retrieves the next n elements in the collection.
helpviewer_keywords: ["IEnumTuningSpaces interface [Microsoft TV Technologies]","Next method","IEnumTuningSpaces.Next","IEnumTuningSpaces::Next","IEnumTuningSpacesNext","Next","Next method [Microsoft TV Technologies]","Next method [Microsoft TV Technologies]","IEnumTuningSpaces interface","mstv.ienumtuningspaces_next","tuner/IEnumTuningSpaces::Next"]
old-location: mstv\ienumtuningspaces_next.htm
tech.root: mstv
ms.assetid: 1220d006-10e9-4e64-8a18-8828b62d5da9
ms.date: 12/05/2018
ms.keywords: IEnumTuningSpaces interface [Microsoft TV Technologies],Next method, IEnumTuningSpaces.Next, IEnumTuningSpaces::Next, IEnumTuningSpacesNext, Next, Next method [Microsoft TV Technologies], Next method [Microsoft TV Technologies],IEnumTuningSpaces interface, mstv.ienumtuningspaces_next, tuner/IEnumTuningSpaces::Next
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
 - IEnumTuningSpaces::Next
 - tuner/IEnumTuningSpaces::Next
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
 - IEnumTuningSpaces.Next
---

# IEnumTuningSpaces::Next


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Next</b> method retrieves the next n elements in the collection.

## -parameters

### -param celt [in]

The number of elements to retrieve.

### -param rgelt [out]

Address of an array of <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace</a> interface pointers that will receive the retrieved Tuning Space objects.

### -param pceltFetched [out]

Receives the number of elements actually retrieved.

## -returns

Returns S_OK if successful. This method will succeed even if <i>celt</i> is zero. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ienumtuningspaces">IEnumTuningSpaces Interface</a>