---
UID: NF:tuner.ITuningSpace.put_DefaultLocator
title: ITuningSpace::put_DefaultLocator (tuner.h)
description: The put_DefaultLocator method sets the default locator for this tuning space.
helpviewer_keywords: ["ITuningSpace interface [Microsoft TV Technologies]","put_DefaultLocator method","ITuningSpace.put_DefaultLocator","ITuningSpace::put_DefaultLocator","ITuningSpaceput_DefaultLocator","mstv.ituningspace_put_defaultlocator","put_DefaultLocator","put_DefaultLocator method [Microsoft TV Technologies]","put_DefaultLocator method [Microsoft TV Technologies]","ITuningSpace interface","tuner/ITuningSpace::put_DefaultLocator"]
old-location: mstv\ituningspace_put_defaultlocator.htm
tech.root: mstv
ms.assetid: 59065cc9-8a11-4551-ad3d-e7963628aa20
ms.date: 12/05/2018
ms.keywords: ITuningSpace interface [Microsoft TV Technologies],put_DefaultLocator method, ITuningSpace.put_DefaultLocator, ITuningSpace::put_DefaultLocator, ITuningSpaceput_DefaultLocator, mstv.ituningspace_put_defaultlocator, put_DefaultLocator, put_DefaultLocator method [Microsoft TV Technologies], put_DefaultLocator method [Microsoft TV Technologies],ITuningSpace interface, tuner/ITuningSpace::put_DefaultLocator
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
 - ITuningSpace::put_DefaultLocator
 - tuner/ITuningSpace::put_DefaultLocator
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
 - ITuningSpace.put_DefaultLocator
---

# ITuningSpace::put_DefaultLocator


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_DefaultLocator</b> method sets the default locator for this tuning space.

## -parameters

### -param LocatorVal [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ilocator">ILocator</a> interface of the locator object.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

See <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspace-get_defaultlocator">ITuningSpace::get_DefaultLocator</a> for more information about the default locator.

For DVB tuning spaces, the sytem type (cable, terrestrial, or satellite) of the tuning space must match the locator object. Otherwise, the method returns DISP_E_TYPEMISMATCH. For more information, see <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbtuningspace-put_systemtype">IDVBTuningSpace::put_SystemType</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace Interface</a>