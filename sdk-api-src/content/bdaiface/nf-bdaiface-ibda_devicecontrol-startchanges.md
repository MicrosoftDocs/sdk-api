---
UID: NF:bdaiface.IBDA_DeviceControl.StartChanges
title: IBDA_DeviceControl::StartChanges (bdaiface.h)
description: The StartChanges method is called by a Network Provider before it begins to modify a set of properties on a BDA device filter.
old-location: mstv\ibda_devicecontrol_startchanges.htm
tech.root: mstv
ms.assetid: 989cdd9b-ea5b-4a80-b157-9469a210b966
ms.date: 12/05/2018
ms.keywords: IBDA_DeviceControl interface [Microsoft TV Technologies],StartChanges method, IBDA_DeviceControl.StartChanges, IBDA_DeviceControl::StartChanges, IBDA_DeviceControlStartChanges, StartChanges, StartChanges method [Microsoft TV Technologies], StartChanges method [Microsoft TV Technologies],IBDA_DeviceControl interface, bdaiface/IBDA_DeviceControl::StartChanges, mstv.ibda_devicecontrol_startchanges
ms.topic: method
f1_keywords:
- bdaiface/IBDA_DeviceControl.StartChanges
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nn-bdaiface-ibda_devicecontrol">IBDA_DeviceControl Interface</a>
 

 

