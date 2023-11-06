---
UID: NF:tuner.IDVBTLocator.put_LPInnerFEC
title: IDVBTLocator::put_LPInnerFEC (tuner.h)
description: The put_LPInnerFEC method sets the inner FEC type of the low-priority stream.
helpviewer_keywords: ["IDVBTLocator interface [Microsoft TV Technologies]","put_LPInnerFEC method","IDVBTLocator.put_LPInnerFEC","IDVBTLocator::put_LPInnerFEC","IDVBTLocatorput_LPInnerFEC","mstv.idvbtlocator_put_lpinnerfec","put_LPInnerFEC","put_LPInnerFEC method [Microsoft TV Technologies]","put_LPInnerFEC method [Microsoft TV Technologies]","IDVBTLocator interface","tuner/IDVBTLocator::put_LPInnerFEC"]
old-location: mstv\idvbtlocator_put_lpinnerfec.htm
tech.root: mstv
ms.assetid: 37b5b063-a0ae-4ef8-a63b-44c009a31eb8
ms.date: 12/05/2018
ms.keywords: IDVBTLocator interface [Microsoft TV Technologies],put_LPInnerFEC method, IDVBTLocator.put_LPInnerFEC, IDVBTLocator::put_LPInnerFEC, IDVBTLocatorput_LPInnerFEC, mstv.idvbtlocator_put_lpinnerfec, put_LPInnerFEC, put_LPInnerFEC method [Microsoft TV Technologies], put_LPInnerFEC method [Microsoft TV Technologies],IDVBTLocator interface, tuner/IDVBTLocator::put_LPInnerFEC
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
 - IDVBTLocator::put_LPInnerFEC
 - tuner/IDVBTLocator::put_LPInnerFEC
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
 - IDVBTLocator.put_LPInnerFEC
---

# IDVBTLocator::put_LPInnerFEC


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_LPInnerFEC</b> method sets the inner FEC type of the low-priority stream.

## -parameters

### -param FEC [in]

Variable of type <a href="/previous-versions/windows/desktop/mstv/fecmethod">FECMethod</a> that specifies the FEC type.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbtlocator">IDVBTLocator Interface</a>