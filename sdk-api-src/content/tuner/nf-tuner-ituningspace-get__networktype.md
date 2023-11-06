---
UID: NF:tuner.ITuningSpace.get__NetworkType
title: ITuningSpace::get__NetworkType (tuner.h)
description: The get_NetworkType method retrieves the network type for this tuning space.
helpviewer_keywords: ["ITuningSpace interface [Microsoft TV Technologies]","get__NetworkType method","ITuningSpace.get__NetworkType","ITuningSpace::get__NetworkType","ITuningSpaceget__NetworkType","get__NetworkType","get__NetworkType method [Microsoft TV Technologies]","get__NetworkType method [Microsoft TV Technologies]","ITuningSpace interface","mstv.ituningspace_get__networktype","tuner/ITuningSpace::get__NetworkType"]
old-location: mstv\ituningspace_get__networktype.htm
tech.root: mstv
ms.assetid: 54cf0c5b-03fb-4419-976c-acc821dfc7e8
ms.date: 12/05/2018
ms.keywords: ITuningSpace interface [Microsoft TV Technologies],get__NetworkType method, ITuningSpace.get__NetworkType, ITuningSpace::get__NetworkType, ITuningSpaceget__NetworkType, get__NetworkType, get__NetworkType method [Microsoft TV Technologies], get__NetworkType method [Microsoft TV Technologies],ITuningSpace interface, mstv.ituningspace_get__networktype, tuner/ITuningSpace::get__NetworkType
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
 - ITuningSpace::get__NetworkType
 - tuner/ITuningSpace::get__NetworkType
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
 - ITuningSpace.get__NetworkType
---

# ITuningSpace::get__NetworkType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_NetworkType</b> method retrieves the network type for this tuning space.

## -parameters

### -param NetworkTypeGuid [out]

Pointer to a variable that receives the network type GUID. This GUID corresponds to the CLSID of the Network Provider for the tuning space. For some tuning spaces, the network type is GUID_NULL, which means the tuning space does not use a Network Provider filter.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace Interface</a>