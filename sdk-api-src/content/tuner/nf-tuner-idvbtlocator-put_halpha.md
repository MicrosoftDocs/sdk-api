---
UID: NF:tuner.IDVBTLocator.put_HAlpha
title: IDVBTLocator::put_HAlpha (tuner.h)
description: The put_HAlpha method sets the hierarchy alpha.
helpviewer_keywords: ["IDVBTLocator interface [Microsoft TV Technologies]","put_HAlpha method","IDVBTLocator.put_HAlpha","IDVBTLocator::put_HAlpha","IDVBTLocatorput_HAlpha","mstv.idvbtlocator_put_halpha","put_HAlpha","put_HAlpha method [Microsoft TV Technologies]","put_HAlpha method [Microsoft TV Technologies]","IDVBTLocator interface","tuner/IDVBTLocator::put_HAlpha"]
old-location: mstv\idvbtlocator_put_halpha.htm
tech.root: mstv
ms.assetid: 2f444c28-972e-4e90-ad99-8bc4f4ee25b7
ms.date: 12/05/2018
ms.keywords: IDVBTLocator interface [Microsoft TV Technologies],put_HAlpha method, IDVBTLocator.put_HAlpha, IDVBTLocator::put_HAlpha, IDVBTLocatorput_HAlpha, mstv.idvbtlocator_put_halpha, put_HAlpha, put_HAlpha method [Microsoft TV Technologies], put_HAlpha method [Microsoft TV Technologies],IDVBTLocator interface, tuner/IDVBTLocator::put_HAlpha
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
 - IDVBTLocator::put_HAlpha
 - tuner/IDVBTLocator::put_HAlpha
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
 - IDVBTLocator.put_HAlpha
---

# IDVBTLocator::put_HAlpha


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_HAlpha</b> method sets the hierarchy alpha.

## -parameters

### -param Alpha [in]

Variable of type <a href="/previous-versions/windows/desktop/mstv/hierarchyalpha">HierarchyAlpha</a> that specifies the hierarchy alpha.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbtlocator">IDVBTLocator Interface</a>