---
UID: NF:bdaiface.IBDA_DeviceControl.StartChanges
title: IBDA_DeviceControl::StartChanges
author: windows-sdk-content
description: The StartChanges method is called by a Network Provider before it begins to modify a set of properties on a BDA device filter.
old-location: mstv\ibda_devicecontrol_startchanges.htm
tech.root: mstv
ms.assetid: 989cdd9b-ea5b-4a80-b157-9469a210b966
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IBDA_DeviceControl interface [Microsoft TV Technologies],StartChanges method, IBDA_DeviceControl.StartChanges, IBDA_DeviceControl::StartChanges, IBDA_DeviceControlStartChanges, StartChanges, StartChanges method [Microsoft TV Technologies], StartChanges method [Microsoft TV Technologies],IBDA_DeviceControl interface, bdaiface/IBDA_DeviceControl::StartChanges, mstv.ibda_devicecontrol_startchanges
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
 - IBDA_DeviceControl.StartChanges
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- bdaiface.h
: 
- IBDA_DeviceControl.StartChanges
: 
---

# IBDA_DeviceControl::StartChanges


## -description



The <b>StartChanges</b> method is called by a Network Provider before it begins to modify a set of properties on a BDA device filter.




## -parameters






## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The device filter validates and accumulates all changes requested after <b>StartChanges</b>. It makes the accumulated list of changes when <b>CommitChanges</b> is called.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/41e167b0-100e-41d2-8759-0411a10931ae">IBDA_DeviceControl Interface</a>
 

 

