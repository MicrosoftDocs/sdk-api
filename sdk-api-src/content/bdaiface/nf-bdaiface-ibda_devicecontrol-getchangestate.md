---
UID: NF:bdaiface.IBDA_DeviceControl.GetChangeState
title: IBDA_DeviceControl::GetChangeState
author: windows-sdk-content
description: The GetChangeState method returns a value indicating whether any uncommitted changes are currently pending in the filter.
old-location: mstv\ibda_devicecontrol_getchangestate.htm
tech.root: MSTV
ms.assetid: 17a36763-552a-44dc-8068-90f1b8fe09e5
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetChangeState, GetChangeState method [Microsoft TV Technologies], GetChangeState method [Microsoft TV Technologies],IBDA_DeviceControl interface, IBDA_DeviceControl interface [Microsoft TV Technologies],GetChangeState method, IBDA_DeviceControl.GetChangeState, IBDA_DeviceControl::GetChangeState, IBDA_DeviceControlGetChangeState, bdaiface/IBDA_DeviceControl::GetChangeState, mstv.ibda_devicecontrol_getchangestate
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693278(v=VS.85).aspx">IBDA_DeviceControl Interface</a>
 

 

