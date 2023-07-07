---
UID: NF:tuner.ILocator.get_SymbolRate
title: ILocator::get_SymbolRate (tuner.h)
description: The get_SymbolRate method gets the QPSK symbol rate.
helpviewer_keywords: ["IDigitalLocatorget_SymbolRate","ILocator interface [Microsoft TV Technologies]","get_SymbolRate method","ILocator.get_SymbolRate","ILocator::get_SymbolRate","get_SymbolRate","get_SymbolRate method [Microsoft TV Technologies]","get_SymbolRate method [Microsoft TV Technologies]","ILocator interface","mstv.ilocator_get_symbolrate","tuner/ILocator::get_SymbolRate"]
old-location: mstv\ilocator_get_symbolrate.htm
tech.root: mstv
ms.assetid: 828967df-6ce1-4320-ae83-7bfaec79f8c7
ms.date: 12/05/2018
ms.keywords: IDigitalLocatorget_SymbolRate, ILocator interface [Microsoft TV Technologies],get_SymbolRate method, ILocator.get_SymbolRate, ILocator::get_SymbolRate, get_SymbolRate, get_SymbolRate method [Microsoft TV Technologies], get_SymbolRate method [Microsoft TV Technologies],ILocator interface, mstv.ilocator_get_symbolrate, tuner/ILocator::get_SymbolRate
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - ILocator::get_SymbolRate
 - tuner/ILocator::get_SymbolRate
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
 - ILocator.get_SymbolRate
---

# ILocator::get_SymbolRate


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_SymbolRate</b> method gets the QPSK symbol rate.

## -parameters

### -param Rate [out]

Receives the QPSK symbol rate. The rate is expressed in symbols per second.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ilocator">ILocator</a>



<a href="/previous-versions/dd693589(v=vs.85)">put_SymbolRate</a>