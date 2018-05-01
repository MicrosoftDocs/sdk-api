---
UID: NI:emi.IOCTL_EMI_GET_MEASUREMENT
title: IOCTL_EMI_GET_MEASUREMENT
author: windows-driver-content
description: The IOCTL_EMI_GET_MEASUREMENT control code retrieves the current energy measurement and the time at which the measurement was taken.
old-location: powermeter\ioctl_emi_get_measurement.htm
old-project: powermeter
ms.assetid: E23B1ED2-A87D-419A-8BEB-136AA77258AE
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IOCTL_EMI_GET_MEASUREMENT, IOCTL_EMI_GET_MEASUREMENT control code [Power Metering and Budgeting Devices], emi/IOCTL_EMI_GET_MEASUREMENT, powermeter.ioctl_emi_get_measurement
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: emi.h
req.include-header: Emi.h
req.target-type: Windows
req.target-min-winverclnt: Available starting with Windows 10.
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
req.typenames: EMI_MEASUREMENT_UNIT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	emi.h
api_name:
-	IOCTL_EMI_GET_MEASUREMENT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IOCTL_EMI_GET_MEASUREMENT IOCTL


## -description


The <b>IOCTL_EMI_GET_MEASUREMENT</b> 
   control code retrieves the current energy measurement and the time at which the measurement was taken. 


## -ioctlparameters




### -input-buffer



<text></text>




### -input-buffer-length



<text></text>




### -output-buffer



<text></text>




### -output-buffer-length



<text></text>




### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block



Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.

Otherwise, Status to the appropriate error condition as a NTSTATUS code. 

For more information, see [NTSTATUS Values](https://docs.microsoft.com/en-us/windows-hardware/drivers/kernel/ntstatus-values).




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn957431">Energy Metering Interface</a>
 

 

