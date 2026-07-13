---
UID: NF:bdaiface.IBDA_SignalProperties.GetNetworkType
title: IBDA_SignalProperties::GetNetworkType (bdaiface.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetNetworkType","GetNetworkType method [Microsoft TV Technologies]","GetNetworkType method [Microsoft TV Technologies]","IBDA_SignalProperties interface","IBDA_SignalProperties interface [Microsoft TV Technologies]","GetNetworkType method","IBDA_SignalProperties.GetNetworkType","IBDA_SignalProperties::GetNetworkType","IBDA_SignalPropertiesGetNetworkType","bdaiface/IBDA_SignalProperties::GetNetworkType","mstv.ibda_signalproperties_getnetworktype"]
old-location: mstv\ibda_signalproperties_getnetworktype.htm
tech.root: mstv
ms.assetid: 6c799cad-2371-4845-a783-e7227fb81c4c
ms.date: 12/05/2018
ms.keywords: GetNetworkType, GetNetworkType method [Microsoft TV Technologies], GetNetworkType method [Microsoft TV Technologies],IBDA_SignalProperties interface, IBDA_SignalProperties interface [Microsoft TV Technologies],GetNetworkType method, IBDA_SignalProperties.GetNetworkType, IBDA_SignalProperties::GetNetworkType, IBDA_SignalPropertiesGetNetworkType, bdaiface/IBDA_SignalProperties::GetNetworkType, mstv.ibda_signalproperties_getnetworktype
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
 - IBDA_SignalProperties::GetNetworkType
 - bdaiface/IBDA_SignalProperties::GetNetworkType
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
 - IBDA_SignalProperties.GetNetworkType
---

# IBDA_SignalProperties::GetNetworkType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetNetworkType</b> method retrieves the network type for the current tuning request.

## -parameters

### -param pguidNetworkType [in, out]

Receives a GUID identifying the network type.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_signalproperties">IBDA_SignalProperties Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_signalproperties-putnetworktype">PutNetworkType</a>