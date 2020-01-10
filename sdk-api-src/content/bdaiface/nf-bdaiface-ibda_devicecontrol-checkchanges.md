---
UID: NF:bdaiface.IBDA_DeviceControl.CheckChanges
title: IBDA_DeviceControl::CheckChanges (bdaiface.h)
description: The CheckChanges method queries the device filter as to whether the changes that are pending would succeed if they were committed.
old-location: mstv\ibda_devicecontrol_checkchanges.htm
tech.root: mstv
ms.assetid: e4654041-d17b-4b1b-9d0f-23c00b0090ea
ms.date: 12/05/2018
ms.keywords: CheckChanges, CheckChanges method [Microsoft TV Technologies], CheckChanges method [Microsoft TV Technologies],IBDA_DeviceControl interface, IBDA_DeviceControl interface [Microsoft TV Technologies],CheckChanges method, IBDA_DeviceControl.CheckChanges, IBDA_DeviceControl::CheckChanges, IBDA_DeviceControlCheckChanges, bdaiface/IBDA_DeviceControl::CheckChanges, mstv.ibda_devicecontrol_checkchanges
f1_keywords:
- bdaiface/IBDA_DeviceControl.CheckChanges
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
- IBDA_DeviceControl.CheckChanges
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBDA_DeviceControl::CheckChanges


## -description



The <b>CheckChanges</b> method queries the device filter as to whether the changes that are pending would succeed if they were committed.




## -parameters






## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method provides a means to determine whether a particular set of changes would be successful, without actually modifying any parameters on the device.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nn-bdaiface-ibda_devicecontrol">IBDA_DeviceControl Interface</a>
 

 

