---
UID: NF:bdaiface.IBDA_DeviceControl.CheckChanges
title: IBDA_DeviceControl::CheckChanges
author: windows-driver-content
description: The CheckChanges method queries the device filter as to whether the changes that are pending would succeed if they were committed.
old-location: mstv\ibda_devicecontrol_checkchanges.htm
old-project: mstv
ms.assetid: e4654041-d17b-4b1b-9d0f-23c00b0090ea
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: CheckChanges, CheckChanges method [Microsoft TV Technologies], CheckChanges method [Microsoft TV Technologies],IBDA_DeviceControl interface, IBDA_DeviceControl interface [Microsoft TV Technologies],CheckChanges method, IBDA_DeviceControl.CheckChanges, IBDA_DeviceControl::CheckChanges, IBDA_DeviceControlCheckChanges, bdaiface/IBDA_DeviceControl::CheckChanges, mstv.ibda_devicecontrol_checkchanges
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
req.typenames: UICloseReasonType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	bdaiface.h
api_name:
-	IBDA_DeviceControl.CheckChanges
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/41e167b0-100e-41d2-8759-0411a10931ae">IBDA_DeviceControl Interface</a>
 

 

