---
UID: NF:tuner.IDVBSTuningSpace.put_InputRange
title: IDVBSTuningSpace::put_InputRange (tuner.h)
description: The put_InputRange method sets a value indicating which option or switch contains the requested signal source.
helpviewer_keywords: ["IDVBSTuningSpace interface [Microsoft TV Technologies]","put_InputRange method","IDVBSTuningSpace.put_InputRange","IDVBSTuningSpace::put_InputRange","IDVBSTuningSpaceput_InputRange","mstv.idvbstuningspace_put_inputrange","put_InputRange","put_InputRange method [Microsoft TV Technologies]","put_InputRange method [Microsoft TV Technologies]","IDVBSTuningSpace interface","tuner/IDVBSTuningSpace::put_InputRange"]
old-location: mstv\idvbstuningspace_put_inputrange.htm
tech.root: mstv
ms.assetid: fa7c065e-91c7-4780-a33a-c5f6bf77a2c4
ms.date: 12/05/2018
ms.keywords: IDVBSTuningSpace interface [Microsoft TV Technologies],put_InputRange method, IDVBSTuningSpace.put_InputRange, IDVBSTuningSpace::put_InputRange, IDVBSTuningSpaceput_InputRange, mstv.idvbstuningspace_put_inputrange, put_InputRange, put_InputRange method [Microsoft TV Technologies], put_InputRange method [Microsoft TV Technologies],IDVBSTuningSpace interface, tuner/IDVBSTuningSpace::put_InputRange
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
 - IDVBSTuningSpace::put_InputRange
 - tuner/IDVBSTuningSpace::put_InputRange
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
 - IDVBSTuningSpace.put_InputRange
---

# IDVBSTuningSpace::put_InputRange


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_InputRange</b> method sets a value indicating which option or switch contains the requested signal source.

## -parameters

### -param InputRange [in]

Specifies which option or switch contains the requested signal source.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbstuningspace">IDVBSTuningSpace Interface</a>