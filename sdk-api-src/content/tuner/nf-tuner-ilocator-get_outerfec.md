---
UID: NF:tuner.ILocator.get_OuterFEC
title: ILocator::get_OuterFEC (tuner.h)
description: The get_OuterFEC method gets the type of outer FEC that is used.
helpviewer_keywords: ["IDigitalLocatorget_OuterFEC","ILocator interface [Microsoft TV Technologies]","get_OuterFEC method","ILocator.get_OuterFEC","ILocator::get_OuterFEC","get_OuterFEC","get_OuterFEC method [Microsoft TV Technologies]","get_OuterFEC method [Microsoft TV Technologies]","ILocator interface","mstv.ilocator_get_outerfec","tuner/ILocator::get_OuterFEC"]
old-location: mstv\ilocator_get_outerfec.htm
tech.root: mstv
ms.assetid: d32937e1-0b8c-485e-8bd0-df15ab2ed373
ms.date: 12/05/2018
ms.keywords: IDigitalLocatorget_OuterFEC, ILocator interface [Microsoft TV Technologies],get_OuterFEC method, ILocator.get_OuterFEC, ILocator::get_OuterFEC, get_OuterFEC, get_OuterFEC method [Microsoft TV Technologies], get_OuterFEC method [Microsoft TV Technologies],ILocator interface, mstv.ilocator_get_outerfec, tuner/ILocator::get_OuterFEC
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
 - ILocator::get_OuterFEC
 - tuner/ILocator::get_OuterFEC
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
 - ILocator.get_OuterFEC
---

# ILocator::get_OuterFEC


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_OuterFEC</b> method gets the type of outer FEC that is used.

## -parameters

### -param FEC [out]

Pointer to a variable of type <a href="/previous-versions/windows/desktop/mstv/fecmethod">FECMethod</a> that receives the type of outer FEC.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ilocator">ILocator</a>



<a href="/previous-versions/dd693580(v=vs.85)">get_InnerFEC</a>



<a href="/previous-versions/dd693583(v=vs.85)">get_OuterFECRate</a>



<a href="/previous-versions/dd693587(v=vs.85)">put_OuterFEC</a>