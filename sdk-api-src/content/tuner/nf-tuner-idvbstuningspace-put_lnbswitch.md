---
UID: NF:tuner.IDVBSTuningSpace.put_LNBSwitch
title: IDVBSTuningSpace::put_LNBSwitch (tuner.h)
description: The put_LNBSwitch method sets the LNB switch frequency.
helpviewer_keywords: ["IDVBSTuningSpace interface [Microsoft TV Technologies]","put_LNBSwitch method","IDVBSTuningSpace.put_LNBSwitch","IDVBSTuningSpace::put_LNBSwitch","IDVBSTuningSpaceput_LNBSwitch","mstv.idvbstuningspace_put_lnbswitch","put_LNBSwitch","put_LNBSwitch method [Microsoft TV Technologies]","put_LNBSwitch method [Microsoft TV Technologies]","IDVBSTuningSpace interface","tuner/IDVBSTuningSpace::put_LNBSwitch"]
old-location: mstv\idvbstuningspace_put_lnbswitch.htm
tech.root: mstv
ms.assetid: 40f9ae9e-ba0d-468d-81c2-4641770e39a5
ms.date: 12/05/2018
ms.keywords: IDVBSTuningSpace interface [Microsoft TV Technologies],put_LNBSwitch method, IDVBSTuningSpace.put_LNBSwitch, IDVBSTuningSpace::put_LNBSwitch, IDVBSTuningSpaceput_LNBSwitch, mstv.idvbstuningspace_put_lnbswitch, put_LNBSwitch, put_LNBSwitch method [Microsoft TV Technologies], put_LNBSwitch method [Microsoft TV Technologies],IDVBSTuningSpace interface, tuner/IDVBSTuningSpace::put_LNBSwitch
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
 - IDVBSTuningSpace::put_LNBSwitch
 - tuner/IDVBSTuningSpace::put_LNBSwitch
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
 - IDVBSTuningSpace.put_LNBSwitch
---

# IDVBSTuningSpace::put_LNBSwitch


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_LNBSwitch</b> method sets the LNB switch frequency.

## -parameters

### -param LNBSwitch [in]

Specifies the LNB switch frequency, in kilohertz (kHz).

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbstuningspace">IDVBSTuningSpace Interface</a>