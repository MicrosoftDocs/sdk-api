---
UID: NF:tuner.ITuningSpace.get_DefaultLocator
title: ITuningSpace::get_DefaultLocator (tuner.h)
description: The get_DefaultLocator method retrieves the default locator for this tuning space.
helpviewer_keywords: ["ITuningSpace interface [Microsoft TV Technologies]","get_DefaultLocator method","ITuningSpace.get_DefaultLocator","ITuningSpace::get_DefaultLocator","ITuningSpaceget_DefaultLocator","get_DefaultLocator","get_DefaultLocator method [Microsoft TV Technologies]","get_DefaultLocator method [Microsoft TV Technologies]","ITuningSpace interface","mstv.ituningspace_get_defaultlocator","tuner/ITuningSpace::get_DefaultLocator"]
old-location: mstv\ituningspace_get_defaultlocator.htm
tech.root: mstv
ms.assetid: facc14bd-182e-4b8e-a567-1bf1d3c4ff36
ms.date: 12/05/2018
ms.keywords: ITuningSpace interface [Microsoft TV Technologies],get_DefaultLocator method, ITuningSpace.get_DefaultLocator, ITuningSpace::get_DefaultLocator, ITuningSpaceget_DefaultLocator, get_DefaultLocator, get_DefaultLocator method [Microsoft TV Technologies], get_DefaultLocator method [Microsoft TV Technologies],ITuningSpace interface, mstv.ituningspace_get_defaultlocator, tuner/ITuningSpace::get_DefaultLocator
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
 - ITuningSpace::get_DefaultLocator
 - tuner/ITuningSpace::get_DefaultLocator
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
 - ITuningSpace.get_DefaultLocator
---

# ITuningSpace::get_DefaultLocator


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_DefaultLocator</b> method retrieves the default locator for this tuning space.

## -parameters

### -param LocatorVal [out]

Address of a variable that receives a pointer to <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ilocator">ILocator</a> interface. The caller must release the interface.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

The tuning space might not have a default locator. It is the application's responsibility to provide a default locator for the tuning space if needed.

If the tuning space does not have a default locator, this method succeeds but returns the value <b>NULL</b> in the <i>ppLocatorVal</i> parameter. Check for a <b>NULL</b> value before attempting to dereference the pointer.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace Interface</a>



<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspace-put_defaultlocator">ITuningSpace::put_DefaultLocator</a>