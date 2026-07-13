---
UID: NF:bdaiface.IBDA_PinControl.GetPinType
title: IBDA_PinControl::GetPinType (bdaiface.h)
description: The GetPinType method retrieves the type of the pin.
helpviewer_keywords: ["GetPinType","GetPinType method [Microsoft TV Technologies]","GetPinType method [Microsoft TV Technologies]","IBDA_PinControl interface","IBDA_PinControl interface [Microsoft TV Technologies]","GetPinType method","IBDA_PinControl.GetPinType","IBDA_PinControl::GetPinType","IBDA_PinControlGetPinType","bdaiface/IBDA_PinControl::GetPinType","mstv.ibda_pincontrol_getpintype"]
old-location: mstv\ibda_pincontrol_getpintype.htm
tech.root: mstv
ms.assetid: 97ab3873-be75-48a5-b854-303aec3d7058
ms.date: 12/05/2018
ms.keywords: GetPinType, GetPinType method [Microsoft TV Technologies], GetPinType method [Microsoft TV Technologies],IBDA_PinControl interface, IBDA_PinControl interface [Microsoft TV Technologies],GetPinType method, IBDA_PinControl.GetPinType, IBDA_PinControl::GetPinType, IBDA_PinControlGetPinType, bdaiface/IBDA_PinControl::GetPinType, mstv.ibda_pincontrol_getpintype
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
 - IBDA_PinControl::GetPinType
 - bdaiface/IBDA_PinControl::GetPinType
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
 - IBDA_PinControl.GetPinType
---

# IBDA_PinControl::GetPinType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetPinType</b> method retrieves the type of the pin.

## -parameters

### -param pulPinType [out]

Pointer that receives the pin type.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_pincontrol">IBDA_PinControl Interface</a>