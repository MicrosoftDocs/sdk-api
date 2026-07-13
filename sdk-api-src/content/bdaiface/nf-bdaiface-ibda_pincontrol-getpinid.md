---
UID: NF:bdaiface.IBDA_PinControl.GetPinID
title: IBDA_PinControl::GetPinID (bdaiface.h)
description: The GetPinID method retrieves the ID of the pin.
helpviewer_keywords: ["GetPinID","GetPinID method [Microsoft TV Technologies]","GetPinID method [Microsoft TV Technologies]","IBDA_PinControl interface","IBDA_PinControl interface [Microsoft TV Technologies]","GetPinID method","IBDA_PinControl.GetPinID","IBDA_PinControl::GetPinID","IBDA_PinControlGetPinID","bdaiface/IBDA_PinControl::GetPinID","mstv.ibda_pincontrol_getpinid"]
old-location: mstv\ibda_pincontrol_getpinid.htm
tech.root: mstv
ms.assetid: 90f6db23-d708-4773-b91a-e4b23d1e3c5b
ms.date: 12/05/2018
ms.keywords: GetPinID, GetPinID method [Microsoft TV Technologies], GetPinID method [Microsoft TV Technologies],IBDA_PinControl interface, IBDA_PinControl interface [Microsoft TV Technologies],GetPinID method, IBDA_PinControl.GetPinID, IBDA_PinControl::GetPinID, IBDA_PinControlGetPinID, bdaiface/IBDA_PinControl::GetPinID, mstv.ibda_pincontrol_getpinid
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
 - IBDA_PinControl::GetPinID
 - bdaiface/IBDA_PinControl::GetPinID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_PinControl.GetPinID
---

# IBDA_PinControl::GetPinID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetPinID</b> method retrieves the ID of the pin.

## -parameters

### -param pulPinID [out]

Pointer that receives the pin's identifier.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_pincontrol">IBDA_PinControl Interface</a>