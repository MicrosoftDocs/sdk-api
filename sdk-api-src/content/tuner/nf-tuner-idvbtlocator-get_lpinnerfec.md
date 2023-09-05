---
UID: NF:tuner.IDVBTLocator.get_LPInnerFEC
title: IDVBTLocator::get_LPInnerFEC (tuner.h)
description: The get_LPInnerFEC method retrieves the inner FEC type of the low-priority stream.
helpviewer_keywords: ["IDVBTLocator interface [Microsoft TV Technologies]","get_LPInnerFEC method","IDVBTLocator.get_LPInnerFEC","IDVBTLocator::get_LPInnerFEC","IDVBTLocatorget_LPInnerFEC","get_LPInnerFEC","get_LPInnerFEC method [Microsoft TV Technologies]","get_LPInnerFEC method [Microsoft TV Technologies]","IDVBTLocator interface","mstv.idvbtlocator_get_lpinnerfec","tuner/IDVBTLocator::get_LPInnerFEC"]
old-location: mstv\idvbtlocator_get_lpinnerfec.htm
tech.root: mstv
ms.assetid: 069904ad-5faa-4ac4-bf30-538284de2de8
ms.date: 12/05/2018
ms.keywords: IDVBTLocator interface [Microsoft TV Technologies],get_LPInnerFEC method, IDVBTLocator.get_LPInnerFEC, IDVBTLocator::get_LPInnerFEC, IDVBTLocatorget_LPInnerFEC, get_LPInnerFEC, get_LPInnerFEC method [Microsoft TV Technologies], get_LPInnerFEC method [Microsoft TV Technologies],IDVBTLocator interface, mstv.idvbtlocator_get_lpinnerfec, tuner/IDVBTLocator::get_LPInnerFEC
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
 - IDVBTLocator::get_LPInnerFEC
 - tuner/IDVBTLocator::get_LPInnerFEC
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
 - IDVBTLocator.get_LPInnerFEC
---

# IDVBTLocator::get_LPInnerFEC


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_LPInnerFEC</b> method retrieves the inner FEC type of the low-priority stream.

## -parameters

### -param FEC [out]

Receives a member of the <a href="/previous-versions/windows/desktop/mstv/fecmethod">FECMethod</a> enumeration.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbtlocator">IDVBTLocator Interface</a>