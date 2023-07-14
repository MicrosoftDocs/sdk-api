---
UID: NF:tuner.IDVBTLocator.get_HAlpha
title: IDVBTLocator::get_HAlpha (tuner.h)
description: The get_HAlpha method retrieves the hierarchy alpha.
helpviewer_keywords: ["IDVBTLocator interface [Microsoft TV Technologies]","get_HAlpha method","IDVBTLocator.get_HAlpha","IDVBTLocator::get_HAlpha","IDVBTLocatorget_HAlpha","get_HAlpha","get_HAlpha method [Microsoft TV Technologies]","get_HAlpha method [Microsoft TV Technologies]","IDVBTLocator interface","mstv.idvbtlocator_get_halpha","tuner/IDVBTLocator::get_HAlpha"]
old-location: mstv\idvbtlocator_get_halpha.htm
tech.root: mstv
ms.assetid: 523222c3-ae40-4eed-af22-6cba56df4959
ms.date: 12/05/2018
ms.keywords: IDVBTLocator interface [Microsoft TV Technologies],get_HAlpha method, IDVBTLocator.get_HAlpha, IDVBTLocator::get_HAlpha, IDVBTLocatorget_HAlpha, get_HAlpha, get_HAlpha method [Microsoft TV Technologies], get_HAlpha method [Microsoft TV Technologies],IDVBTLocator interface, mstv.idvbtlocator_get_halpha, tuner/IDVBTLocator::get_HAlpha
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
 - IDVBTLocator::get_HAlpha
 - tuner/IDVBTLocator::get_HAlpha
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
 - IDVBTLocator.get_HAlpha
---

# IDVBTLocator::get_HAlpha


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_HAlpha</b> method retrieves the hierarchy alpha.

## -parameters

### -param Alpha [out]

Receives a member of the <a href="/previous-versions/windows/desktop/mstv/hierarchyalpha">HierarchyAlpha</a> enumeration.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbtlocator">IDVBTLocator Interface</a>