---
UID: NF:tuner.ILocator.get_Modulation
title: ILocator::get_Modulation (tuner.h)
description: The get_Modulation method gets the modulation type.
helpviewer_keywords: ["ILocator interface [Microsoft TV Technologies]","get_Modulation method","ILocator.get_Modulation","ILocator::get_Modulation","ILocatorget_Modulation","get_Modulation","get_Modulation method [Microsoft TV Technologies]","get_Modulation method [Microsoft TV Technologies]","ILocator interface","mstv.ilocator_get_modulation","tuner/ILocator::get_Modulation"]
old-location: mstv\ilocator_get_modulation.htm
tech.root: mstv
ms.assetid: 6aca60fa-ea8d-440d-a037-20537c25a105
ms.date: 12/05/2018
ms.keywords: ILocator interface [Microsoft TV Technologies],get_Modulation method, ILocator.get_Modulation, ILocator::get_Modulation, ILocatorget_Modulation, get_Modulation, get_Modulation method [Microsoft TV Technologies], get_Modulation method [Microsoft TV Technologies],ILocator interface, mstv.ilocator_get_modulation, tuner/ILocator::get_Modulation
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
 - ILocator::get_Modulation
 - tuner/ILocator::get_Modulation
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
 - ILocator.get_Modulation
---

# ILocator::get_Modulation


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Modulation</b> method gets the modulation type.

## -parameters

### -param Modulation [out]

Receives the modulation type, as a member of the <a href="/previous-versions/windows/desktop/mstv/modulationtype">ModulationType</a> enumeration.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

See <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ilocator-put_modulation">put_Modulation</a> for the definition of <b>ModulationType</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ilocator">ILocator Interface</a>