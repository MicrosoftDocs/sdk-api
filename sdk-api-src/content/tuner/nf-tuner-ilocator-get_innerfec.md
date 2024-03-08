---
UID: NF:tuner.ILocator.get_InnerFEC
title: ILocator::get_InnerFEC (tuner.h)
description: The get_InnerFEC method gets the type of inner FEC that is used.
helpviewer_keywords: ["IDigitalLocatorget_InnerFEC","ILocator interface [Microsoft TV Technologies]","get_InnerFEC method","ILocator.get_InnerFEC","ILocator::get_InnerFEC","get_InnerFEC","get_InnerFEC method [Microsoft TV Technologies]","get_InnerFEC method [Microsoft TV Technologies]","ILocator interface","mstv.ilocator_get_innerfec","tuner/ILocator::get_InnerFEC"]
old-location: mstv\ilocator_get_innerfec.htm
tech.root: mstv
ms.assetid: aaa81a62-7e19-4d71-8378-77d6318a4e84
ms.date: 12/05/2018
ms.keywords: IDigitalLocatorget_InnerFEC, ILocator interface [Microsoft TV Technologies],get_InnerFEC method, ILocator.get_InnerFEC, ILocator::get_InnerFEC, get_InnerFEC, get_InnerFEC method [Microsoft TV Technologies], get_InnerFEC method [Microsoft TV Technologies],ILocator interface, mstv.ilocator_get_innerfec, tuner/ILocator::get_InnerFEC
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
 - ILocator::get_InnerFEC
 - tuner/ILocator::get_InnerFEC
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
 - ILocator.get_InnerFEC
---

# ILocator::get_InnerFEC


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_InnerFEC</b> method gets the type of inner FEC that is used.

## -parameters

### -param FEC [out]

Pointer to a variable of type <a href="/previous-versions/windows/desktop/mstv/fecmethod">FECMethod</a> that receives the type of inner FEC.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ilocator">ILocator</a>



<a href="/previous-versions/dd693581(v=vs.85)">get_InnerFECRate</a>



<a href="/previous-versions/dd693582(v=vs.85)">get_OuterFEC</a>



<a href="/previous-versions/dd693585(v=vs.85)">put_InnerFEC</a>