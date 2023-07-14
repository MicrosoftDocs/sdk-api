---
UID: NF:tuner.ILocator.get_OuterFECRate
title: ILocator::get_OuterFECRate (tuner.h)
description: The get_OuterFECRate method gets the outer FEC rate.
helpviewer_keywords: ["IDigitalLocatorget_OuterFECRate","ILocator interface [Microsoft TV Technologies]","get_OuterFECRate method","ILocator.get_OuterFECRate","ILocator::get_OuterFECRate","get_OuterFECRate","get_OuterFECRate method [Microsoft TV Technologies]","get_OuterFECRate method [Microsoft TV Technologies]","ILocator interface","mstv.ilocator_get_outerfecrate","tuner/ILocator::get_OuterFECRate"]
old-location: mstv\ilocator_get_outerfecrate.htm
tech.root: mstv
ms.assetid: 550103a8-dcf9-4a52-817a-61a589de4299
ms.date: 12/05/2018
ms.keywords: IDigitalLocatorget_OuterFECRate, ILocator interface [Microsoft TV Technologies],get_OuterFECRate method, ILocator.get_OuterFECRate, ILocator::get_OuterFECRate, get_OuterFECRate, get_OuterFECRate method [Microsoft TV Technologies], get_OuterFECRate method [Microsoft TV Technologies],ILocator interface, mstv.ilocator_get_outerfecrate, tuner/ILocator::get_OuterFECRate
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
 - ILocator::get_OuterFECRate
 - tuner/ILocator::get_OuterFECRate
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
 - ILocator.get_OuterFECRate
---

# ILocator::get_OuterFECRate


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_OuterFECRate</b> method gets the outer FEC rate.

## -parameters

### -param FEC [out]

Pointer to a variable of type <a href="/previous-versions/windows/desktop/mstv/binaryconvolutioncoderate">BinaryConvolutionCodeRate</a> that receives the outer FEC rate.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ilocator">ILocator</a>



<a href="/previous-versions/dd693581(v=vs.85)">get_InnerFECRate</a>



<a href="/previous-versions/dd693582(v=vs.85)">get_OuterFEC</a>



<a href="/previous-versions/dd693588(v=vs.85)">put_OuterFECRate</a>