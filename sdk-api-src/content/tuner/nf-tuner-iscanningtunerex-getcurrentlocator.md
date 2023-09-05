---
UID: NF:tuner.IScanningTunerEx.GetCurrentLocator
title: IScanningTunerEx::GetCurrentLocator (tuner.h)
description: This topic applies to Windows Vista and later.
helpviewer_keywords: ["GetCurrentLocator","GetCurrentLocator method [Microsoft TV Technologies]","GetCurrentLocator method [Microsoft TV Technologies]","IScanningTunerEx interface","IScanningTunerEx interface [Microsoft TV Technologies]","GetCurrentLocator method","IScanningTunerEx.GetCurrentLocator","IScanningTunerEx::GetCurrentLocator","IScanningTunerExGetCurrentLocator","mstv.iscanningtunerex_getcurrentlocator","tuner/IScanningTunerEx::GetCurrentLocator"]
old-location: mstv\iscanningtunerex_getcurrentlocator.htm
tech.root: mstv
ms.assetid: f5237236-50f3-49dd-aec0-578e0a8430c2
ms.date: 12/05/2018
ms.keywords: GetCurrentLocator, GetCurrentLocator method [Microsoft TV Technologies], GetCurrentLocator method [Microsoft TV Technologies],IScanningTunerEx interface, IScanningTunerEx interface [Microsoft TV Technologies],GetCurrentLocator method, IScanningTunerEx.GetCurrentLocator, IScanningTunerEx::GetCurrentLocator, IScanningTunerExGetCurrentLocator, mstv.iscanningtunerex_getcurrentlocator, tuner/IScanningTunerEx::GetCurrentLocator
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IScanningTunerEx::GetCurrentLocator
 - tuner/IScanningTunerEx::GetCurrentLocator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tuner.h
api_name:
 - IScanningTunerEx.GetCurrentLocator
---

# IScanningTunerEx::GetCurrentLocator


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Windows Vista and later.
        



The <b>GetCurrentLocator</b> method retrieves the current locator object.

## -parameters

### -param pILocator [out]

Receives a pointer to the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ilocator">ILocator</a> interface of the locator object. The caller must release the interface.

## -returns

When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iscanningtunerex">IScanningTunerEx Interface</a>