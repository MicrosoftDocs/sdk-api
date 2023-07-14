---
UID: NF:bdaiface.IBDA_SignalProperties.GetSignalSource
title: IBDA_SignalProperties::GetSignalSource (bdaiface.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetSignalSource","GetSignalSource method [Microsoft TV Technologies]","GetSignalSource method [Microsoft TV Technologies]","IBDA_SignalProperties interface","IBDA_SignalProperties interface [Microsoft TV Technologies]","GetSignalSource method","IBDA_SignalProperties.GetSignalSource","IBDA_SignalProperties::GetSignalSource","IBDA_SignalPropertiesGetSignalSource","bdaiface/IBDA_SignalProperties::GetSignalSource","mstv.ibda_signalproperties_getsignalsource"]
old-location: mstv\ibda_signalproperties_getsignalsource.htm
tech.root: mstv
ms.assetid: 929ec042-3f43-468e-944a-919dda3893be
ms.date: 12/05/2018
ms.keywords: GetSignalSource, GetSignalSource method [Microsoft TV Technologies], GetSignalSource method [Microsoft TV Technologies],IBDA_SignalProperties interface, IBDA_SignalProperties interface [Microsoft TV Technologies],GetSignalSource method, IBDA_SignalProperties.GetSignalSource, IBDA_SignalProperties::GetSignalSource, IBDA_SignalPropertiesGetSignalSource, bdaiface/IBDA_SignalProperties::GetSignalSource, mstv.ibda_signalproperties_getsignalsource
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IBDA_SignalProperties::GetSignalSource
 - bdaiface/IBDA_SignalProperties::GetSignalSource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bdaiface.h
api_name:
 - IBDA_SignalProperties.GetSignalSource
---

# IBDA_SignalProperties::GetSignalSource


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetSignalSource</b> method retrieves the signal source for the current tuning request.

## -parameters

### -param pulSignalSource [in, out]

Receives a value identifying the signal source. The value is an arbitrary identifier set by the network provider. If two tuners share the same signal source, they should have the same identifier.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

This method returns whatever value was last set by calling <a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_signalproperties-putsignalsource">IBDA_SignalProperties::PutSignalSource</a>.

<div class="alert"><b>Note</b>  The <i>pulSignalSource</i> parameter is marked in the IDL file as [in, out] but is used as an [out] parameter. To preserve binary compatibility with previous versions, it has not been changed.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_signalproperties">IBDA_SignalProperties Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_signalproperties-putsignalsource">PutSignalSource</a>