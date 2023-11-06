---
UID: NF:tuner.ITuningSpace.Clone
title: ITuningSpace::Clone (tuner.h)
description: The Clone method creates a new copy of the tuning space.
helpviewer_keywords: ["Clone","Clone method [Microsoft TV Technologies]","Clone method [Microsoft TV Technologies]","ITuningSpace interface","ITuningSpace interface [Microsoft TV Technologies]","Clone method","ITuningSpace.Clone","ITuningSpace::Clone","ITuningSpaceClone","mstv.ituningspace_clone","tuner/ITuningSpace::Clone"]
old-location: mstv\ituningspace_clone.htm
tech.root: mstv
ms.assetid: 01dcde87-b043-491e-b5cf-9800c12b5335
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Microsoft TV Technologies], Clone method [Microsoft TV Technologies],ITuningSpace interface, ITuningSpace interface [Microsoft TV Technologies],Clone method, ITuningSpace.Clone, ITuningSpace::Clone, ITuningSpaceClone, mstv.ituningspace_clone, tuner/ITuningSpace::Clone
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
 - ITuningSpace::Clone
 - tuner/ITuningSpace::Clone
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
 - ITuningSpace.Clone
---

# ITuningSpace::Clone


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Clone</b> method creates a new copy of the tuning space.

## -parameters

### -param NewTS [out]

Receives a pointer to the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace</a> interface of the new tuning space object. The caller must release the interface.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace Interface</a>