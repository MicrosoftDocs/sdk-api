---
UID: NF:tuner.ILocator.put_OuterFECRate
title: ILocator::put_OuterFECRate (tuner.h)
description: The put_OuterFECRate method sets the outer FEC rate.
helpviewer_keywords: ["IDigitalLocatorput_OuterFECRate","ILocator interface [Microsoft TV Technologies]","put_OuterFECRate method","ILocator.put_OuterFECRate","ILocator::put_OuterFECRate","mstv.ilocator_put_outerfecrate","put_OuterFECRate","put_OuterFECRate method [Microsoft TV Technologies]","put_OuterFECRate method [Microsoft TV Technologies]","ILocator interface","tuner/ILocator::put_OuterFECRate"]
old-location: mstv\ilocator_put_outerfecrate.htm
tech.root: mstv
ms.assetid: 0fd3fa42-4ed6-459b-a6a2-23ed67832780
ms.date: 12/05/2018
ms.keywords: IDigitalLocatorput_OuterFECRate, ILocator interface [Microsoft TV Technologies],put_OuterFECRate method, ILocator.put_OuterFECRate, ILocator::put_OuterFECRate, mstv.ilocator_put_outerfecrate, put_OuterFECRate, put_OuterFECRate method [Microsoft TV Technologies], put_OuterFECRate method [Microsoft TV Technologies],ILocator interface, tuner/ILocator::put_OuterFECRate
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
 - ILocator::put_OuterFECRate
 - tuner/ILocator::put_OuterFECRate
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
 - ILocator.put_OuterFECRate
---

# ILocator::put_OuterFECRate


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_OuterFECRate</b> method sets the outer FEC rate.

## -parameters

### -param FEC [in]

Specifies the outer FEC rate. This parameter is a value of type <a href="/previous-versions/windows/desktop/mstv/binaryconvolutioncoderate">BinaryConvolutionCodeRate</a>.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ilocator">ILocator</a>



<a href="/previous-versions/dd693583(v=vs.85)">get_OuterFECRate</a>



<a href="/previous-versions/dd693586(v=vs.85)">put_InnerFECRate</a>



<a href="/previous-versions/dd693587(v=vs.85)">put_OuterFEC</a>