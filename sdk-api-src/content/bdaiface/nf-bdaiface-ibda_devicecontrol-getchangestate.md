---
UID: NF:bdaiface.IBDA_DeviceControl.GetChangeState
title: IBDA_DeviceControl::GetChangeState (bdaiface.h)
description: The GetChangeState method returns a value indicating whether any uncommitted changes are currently pending in the filter.
helpviewer_keywords: ["GetChangeState","GetChangeState method [Microsoft TV Technologies]","GetChangeState method [Microsoft TV Technologies]","IBDA_DeviceControl interface","IBDA_DeviceControl interface [Microsoft TV Technologies]","GetChangeState method","IBDA_DeviceControl.GetChangeState","IBDA_DeviceControl::GetChangeState","IBDA_DeviceControlGetChangeState","bdaiface/IBDA_DeviceControl::GetChangeState","mstv.ibda_devicecontrol_getchangestate"]
old-location: mstv\ibda_devicecontrol_getchangestate.htm
tech.root: mstv
ms.assetid: 17a36763-552a-44dc-8068-90f1b8fe09e5
ms.date: 12/05/2018
ms.keywords: GetChangeState, GetChangeState method [Microsoft TV Technologies], GetChangeState method [Microsoft TV Technologies],IBDA_DeviceControl interface, IBDA_DeviceControl interface [Microsoft TV Technologies],GetChangeState method, IBDA_DeviceControl.GetChangeState, IBDA_DeviceControl::GetChangeState, IBDA_DeviceControlGetChangeState, bdaiface/IBDA_DeviceControl::GetChangeState, mstv.ibda_devicecontrol_getchangestate
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
 - IBDA_DeviceControl::GetChangeState
 - bdaiface/IBDA_DeviceControl::GetChangeState
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
 - IBDA_DeviceControl.GetChangeState
---

# IBDA_DeviceControl::GetChangeState


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetChangeState</b> method returns a value indicating whether any uncommitted changes are currently pending in the filter.

## -parameters

### -param pState [out]

Receives the current state of the filter. See BDA_CHANGE_STATE in the Windows DDK for possible values.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_devicecontrol">IBDA_DeviceControl Interface</a>