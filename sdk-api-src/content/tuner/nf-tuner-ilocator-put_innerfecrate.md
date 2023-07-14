---
UID: NF:tuner.ILocator.put_InnerFECRate
title: ILocator::put_InnerFECRate (tuner.h)
description: The put_InnerFECRate method sets the inner FEC rate.
helpviewer_keywords: ["IDigitalLocatorput_InnerFECRate","ILocator interface [Microsoft TV Technologies]","put_InnerFECRate method","ILocator.put_InnerFECRate","ILocator::put_InnerFECRate","mstv.ilocator_put_innerfecrate","put_InnerFECRate","put_InnerFECRate method [Microsoft TV Technologies]","put_InnerFECRate method [Microsoft TV Technologies]","ILocator interface","tuner/ILocator::put_InnerFECRate"]
old-location: mstv\ilocator_put_innerfecrate.htm
tech.root: mstv
ms.assetid: 009d1ddf-73ae-432b-adf2-a5a0067345fa
ms.date: 12/05/2018
ms.keywords: IDigitalLocatorput_InnerFECRate, ILocator interface [Microsoft TV Technologies],put_InnerFECRate method, ILocator.put_InnerFECRate, ILocator::put_InnerFECRate, mstv.ilocator_put_innerfecrate, put_InnerFECRate, put_InnerFECRate method [Microsoft TV Technologies], put_InnerFECRate method [Microsoft TV Technologies],ILocator interface, tuner/ILocator::put_InnerFECRate
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
 - ILocator::put_InnerFECRate
 - tuner/ILocator::put_InnerFECRate
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
 - ILocator.put_InnerFECRate
---

# ILocator::put_InnerFECRate


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_InnerFECRate</b> method sets the inner FEC rate.

## -parameters

### -param FEC [in]

Specifies the inner FEC rate. This parameter is a value of type <a href="/previous-versions/windows/desktop/mstv/binaryconvolutioncoderate">BinaryConvolutionCodeRate</a>.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ilocator">ILocator</a>



<a href="/previous-versions/dd693581(v=vs.85)">get_InnerFECRate</a>



<a href="/previous-versions/dd693585(v=vs.85)">put_InnerFEC</a>



<a href="/previous-versions/dd693588(v=vs.85)">put_OuterFECRate</a>