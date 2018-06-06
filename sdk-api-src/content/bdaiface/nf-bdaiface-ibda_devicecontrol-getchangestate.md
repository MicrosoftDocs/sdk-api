---
UID: NF:bdaiface.IBDA_DeviceControl.GetChangeState
title: IBDA_DeviceControl::GetChangeState
author: windows-sdk-content
description: The GetChangeState method returns a value indicating whether any uncommitted changes are currently pending in the filter.
old-location: mstv\ibda_devicecontrol_getchangestate.htm
old-project: mstv
ms.assetid: 17a36763-552a-44dc-8068-90f1b8fe09e5
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetChangeState, GetChangeState method [Microsoft TV Technologies], GetChangeState method [Microsoft TV Technologies],IBDA_DeviceControl interface, IBDA_DeviceControl interface [Microsoft TV Technologies],GetChangeState method, IBDA_DeviceControl.GetChangeState, IBDA_DeviceControl::GetChangeState, IBDA_DeviceControlGetChangeState, bdaiface/IBDA_DeviceControl::GetChangeState, mstv.ibda_devicecontrol_getchangestate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: UICloseReasonType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_DeviceControl.GetChangeState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_DeviceControl::GetChangeState


## -description



The <b>GetChangeState</b> method returns a value indicating whether any uncommitted changes are currently pending in the filter.




## -parameters




### -param pState [out]

Receives the current state of the filter. See BDA_CHANGE_STATE in the Windows DDK for possible values.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/41e167b0-100e-41d2-8759-0411a10931ae">IBDA_DeviceControl Interface</a>
 

 

