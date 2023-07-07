---
UID: NF:tuner.ILocator.put_InnerFEC
title: ILocator::put_InnerFEC (tuner.h)
description: The put_InnerFEC method sets the type of inner FEC to use.
helpviewer_keywords: ["IDigitalLocatorput_InnerFEC","ILocator interface [Microsoft TV Technologies]","put_InnerFEC method","ILocator.put_InnerFEC","ILocator::put_InnerFEC","mstv.ilocator_put_innerfec","put_InnerFEC","put_InnerFEC method [Microsoft TV Technologies]","put_InnerFEC method [Microsoft TV Technologies]","ILocator interface","tuner/ILocator::put_InnerFEC"]
old-location: mstv\ilocator_put_innerfec.htm
tech.root: mstv
ms.assetid: 3ba6cfdf-2095-489c-a899-4b4305758ccb
ms.date: 12/05/2018
ms.keywords: IDigitalLocatorput_InnerFEC, ILocator interface [Microsoft TV Technologies],put_InnerFEC method, ILocator.put_InnerFEC, ILocator::put_InnerFEC, mstv.ilocator_put_innerfec, put_InnerFEC, put_InnerFEC method [Microsoft TV Technologies], put_InnerFEC method [Microsoft TV Technologies],ILocator interface, tuner/ILocator::put_InnerFEC
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
 - ILocator::put_InnerFEC
 - tuner/ILocator::put_InnerFEC
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
 - ILocator.put_InnerFEC
---

# ILocator::put_InnerFEC


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_InnerFEC</b> method sets the type of inner FEC to use.

## -parameters

### -param FEC [in]

Specifies the inner FEC. This parameter is a value of type <a href="/previous-versions/windows/desktop/mstv/fecmethod">FECMethod</a>.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ilocator">ILocator</a>



<a href="/previous-versions/dd693580(v=vs.85)">get_InnerFEC</a>



<a href="/previous-versions/dd693586(v=vs.85)">put_InnerFECRate</a>



<a href="/previous-versions/dd693587(v=vs.85)">put_OuterFEC</a>