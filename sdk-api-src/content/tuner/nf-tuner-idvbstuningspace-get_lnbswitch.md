---
UID: NF:tuner.IDVBSTuningSpace.get_LNBSwitch
title: IDVBSTuningSpace::get_LNBSwitch (tuner.h)
description: The get_LNBSwitch method retrieves the LNB switch.
helpviewer_keywords: ["IDVBSTuningSpace interface [Microsoft TV Technologies]","get_LNBSwitch method","IDVBSTuningSpace.get_LNBSwitch","IDVBSTuningSpace::get_LNBSwitch","IDVBSTuningSpaceget_LNBSwitch","get_LNBSwitch","get_LNBSwitch method [Microsoft TV Technologies]","get_LNBSwitch method [Microsoft TV Technologies]","IDVBSTuningSpace interface","mstv.idvbstuningspace_get_lnbswitch","tuner/IDVBSTuningSpace::get_LNBSwitch"]
old-location: mstv\idvbstuningspace_get_lnbswitch.htm
tech.root: mstv
ms.assetid: 56cea4ef-7679-4b78-883d-194c9259032f
ms.date: 12/05/2018
ms.keywords: IDVBSTuningSpace interface [Microsoft TV Technologies],get_LNBSwitch method, IDVBSTuningSpace.get_LNBSwitch, IDVBSTuningSpace::get_LNBSwitch, IDVBSTuningSpaceget_LNBSwitch, get_LNBSwitch, get_LNBSwitch method [Microsoft TV Technologies], get_LNBSwitch method [Microsoft TV Technologies],IDVBSTuningSpace interface, mstv.idvbstuningspace_get_lnbswitch, tuner/IDVBSTuningSpace::get_LNBSwitch
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
 - IDVBSTuningSpace::get_LNBSwitch
 - tuner/IDVBSTuningSpace::get_LNBSwitch
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
 - IDVBSTuningSpace.get_LNBSwitch
---

# IDVBSTuningSpace::get_LNBSwitch


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_LNBSwitch</b> method retrieves the LNB switch.

## -parameters

### -param LNBSwitch [out]

Receives the LNB switch frequency, in kilohertz (kHz).

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbstuningspace">IDVBSTuningSpace Interface</a>