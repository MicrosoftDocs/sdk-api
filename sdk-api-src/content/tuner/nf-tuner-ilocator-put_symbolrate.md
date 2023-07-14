---
UID: NF:tuner.ILocator.put_SymbolRate
title: ILocator::put_SymbolRate (tuner.h)
description: The put_SymbolRate method sets the QPSK symbol rate.
helpviewer_keywords: ["IDigitalLocatorput_SymbolRate","ILocator interface [Microsoft TV Technologies]","put_SymbolRate method","ILocator.put_SymbolRate","ILocator::put_SymbolRate","mstv.ilocator_put_symbolrate","put_SymbolRate","put_SymbolRate method [Microsoft TV Technologies]","put_SymbolRate method [Microsoft TV Technologies]","ILocator interface","tuner/ILocator::put_SymbolRate"]
old-location: mstv\ilocator_put_symbolrate.htm
tech.root: mstv
ms.assetid: 1eb91e22-b9b1-47dc-a2e4-cc64eeaacaaa
ms.date: 12/05/2018
ms.keywords: IDigitalLocatorput_SymbolRate, ILocator interface [Microsoft TV Technologies],put_SymbolRate method, ILocator.put_SymbolRate, ILocator::put_SymbolRate, mstv.ilocator_put_symbolrate, put_SymbolRate, put_SymbolRate method [Microsoft TV Technologies], put_SymbolRate method [Microsoft TV Technologies],ILocator interface, tuner/ILocator::put_SymbolRate
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
 - ILocator::put_SymbolRate
 - tuner/ILocator::put_SymbolRate
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
 - ILocator.put_SymbolRate
---

# ILocator::put_SymbolRate


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_SymbolRate</b> method sets the QPSK symbol rate.

## -parameters

### -param Rate [in]

Specifies the QPSK symbol rate. The rate is expressed in symbols per second.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ilocator">ILocator</a>



<a href="/previous-versions/dd693584(v=vs.85)">get_SymbolRate</a>