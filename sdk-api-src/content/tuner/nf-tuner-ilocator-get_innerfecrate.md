---
UID: NF:tuner.ILocator.get_InnerFECRate
title: ILocator::get_InnerFECRate (tuner.h)
description: The get_InnerFECRate method gets the inner FEC rate.
helpviewer_keywords: ["IDigitalLocatorget_InnerFECRate","ILocator interface [Microsoft TV Technologies]","get_InnerFECRate method","ILocator.get_InnerFECRate","ILocator::get_InnerFECRate","get_InnerFECRate","get_InnerFECRate method [Microsoft TV Technologies]","get_InnerFECRate method [Microsoft TV Technologies]","ILocator interface","mstv.ilocator_get_innerfecrate","tuner/ILocator::get_InnerFECRate"]
old-location: mstv\ilocator_get_innerfecrate.htm
tech.root: mstv
ms.assetid: d9600c31-9a95-4955-8f8c-542760631050
ms.date: 12/05/2018
ms.keywords: IDigitalLocatorget_InnerFECRate, ILocator interface [Microsoft TV Technologies],get_InnerFECRate method, ILocator.get_InnerFECRate, ILocator::get_InnerFECRate, get_InnerFECRate, get_InnerFECRate method [Microsoft TV Technologies], get_InnerFECRate method [Microsoft TV Technologies],ILocator interface, mstv.ilocator_get_innerfecrate, tuner/ILocator::get_InnerFECRate
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
 - ILocator::get_InnerFECRate
 - tuner/ILocator::get_InnerFECRate
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
 - ILocator.get_InnerFECRate
---

# ILocator::get_InnerFECRate


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_InnerFECRate</b> method gets the inner FEC rate.

## -parameters

### -param FEC [out]

Pointer to a variable of type <a href="/previous-versions/windows/desktop/mstv/binaryconvolutioncoderate">BinaryConvolutionCodeRate</a> that receives the inner FEC rate.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ilocator">ILocator</a>



<a href="/previous-versions/dd693580(v=vs.85)">get_InnerFEC</a>



<a href="/previous-versions/dd693583(v=vs.85)">get_OuterFECRate</a>



<a href="/previous-versions/dd693586(v=vs.85)">put_InnerFECRate</a>