---
UID: NF:tuner.IDVBSTuningSpace.get_InputRange
title: IDVBSTuningSpace::get_InputRange (tuner.h)
description: The get_InputRange method retrieves an integer indicating which option or switch contains the requested signal source.
helpviewer_keywords: ["IDVBSTuningSpace interface [Microsoft TV Technologies]","get_InputRange method","IDVBSTuningSpace.get_InputRange","IDVBSTuningSpace::get_InputRange","IDVBSTuningSpaceget_InputRange","get_InputRange","get_InputRange method [Microsoft TV Technologies]","get_InputRange method [Microsoft TV Technologies]","IDVBSTuningSpace interface","mstv.idvbstuningspace_get_inputrange","tuner/IDVBSTuningSpace::get_InputRange"]
old-location: mstv\idvbstuningspace_get_inputrange.htm
tech.root: mstv
ms.assetid: d116c1d1-df48-434b-ad49-eabd0efaa810
ms.date: 12/05/2018
ms.keywords: IDVBSTuningSpace interface [Microsoft TV Technologies],get_InputRange method, IDVBSTuningSpace.get_InputRange, IDVBSTuningSpace::get_InputRange, IDVBSTuningSpaceget_InputRange, get_InputRange, get_InputRange method [Microsoft TV Technologies], get_InputRange method [Microsoft TV Technologies],IDVBSTuningSpace interface, mstv.idvbstuningspace_get_inputrange, tuner/IDVBSTuningSpace::get_InputRange
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
 - IDVBSTuningSpace::get_InputRange
 - tuner/IDVBSTuningSpace::get_InputRange
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
 - IDVBSTuningSpace.get_InputRange
---

# IDVBSTuningSpace::get_InputRange


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_InputRange</b> method retrieves an integer indicating which option or switch contains the requested signal source.

## -parameters

### -param InputRange [out]

Receives the input range.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbstuningspace">IDVBSTuningSpace Interface</a>