---
UID: NF:bdaiface.IBDA_PinControl.RegistrationContext
title: IBDA_PinControl::RegistrationContext (bdaiface.h)
description: The RegistrationContext method retrieves the registration context of a particular pin.
helpviewer_keywords: ["IBDA_PinControl interface [Microsoft TV Technologies]","RegistrationContext method","IBDA_PinControl.RegistrationContext","IBDA_PinControl::RegistrationContext","IBDA_PinControlRegistrationContext","RegistrationContext","RegistrationContext method [Microsoft TV Technologies]","RegistrationContext method [Microsoft TV Technologies]","IBDA_PinControl interface","bdaiface/IBDA_PinControl::RegistrationContext","mstv.ibda_pincontrol_registrationcontext"]
old-location: mstv\ibda_pincontrol_registrationcontext.htm
tech.root: mstv
ms.assetid: 6e54bb4e-9c65-4f57-ba4a-c5b35ccaae1f
ms.date: 12/05/2018
ms.keywords: IBDA_PinControl interface [Microsoft TV Technologies],RegistrationContext method, IBDA_PinControl.RegistrationContext, IBDA_PinControl::RegistrationContext, IBDA_PinControlRegistrationContext, RegistrationContext, RegistrationContext method [Microsoft TV Technologies], RegistrationContext method [Microsoft TV Technologies],IBDA_PinControl interface, bdaiface/IBDA_PinControl::RegistrationContext, mstv.ibda_pincontrol_registrationcontext
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
 - IBDA_PinControl::RegistrationContext
 - bdaiface/IBDA_PinControl::RegistrationContext
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
 - IBDA_PinControl.RegistrationContext
---

# IBDA_PinControl::RegistrationContext


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>RegistrationContext</b> method retrieves the registration context of a particular pin.

## -parameters

### -param pulRegistrationCtx [out]

Pointer that receives the registration context.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

The registration context uniquely identifies an instance of a particular pin. A Network Provider does not modify this value; it simply retains it in order to keep track of the pins in the graph.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_pincontrol">IBDA_PinControl Interface</a>