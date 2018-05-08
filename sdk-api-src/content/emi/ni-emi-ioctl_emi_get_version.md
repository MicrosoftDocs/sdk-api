---
UID: NI:emi.IOCTL_EMI_GET_VERSION
title: IOCTL_EMI_GET_VERSION
author: windows-driver-content
description: The IOCTL_EMI_GET_VERSION control code retrieves the current version of the EMI interface supported by the device.
old-location: powermeter\ioctl_emi_get_version.htm
old-project: powermeter
ms.assetid: 6B27B70C-DB3C-4EF9-B8FF-8074B0285F87
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IOCTL_EMI_GET_VERSION, IOCTL_EMI_GET_VERSION control, IOCTL_EMI_GET_VERSION control code [Power Metering and Budgeting Devices], emi/IOCTL_EMI_GET_VERSION, powermeter.ioctl_emi_get_version
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
-	IOCTL_EMI_GET_VERSION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IOCTL_EMI_GET_VERSION IOCTL


## -description


The <b>IOCTL_EMI_GET_VERSION</b> 
   control code retrieves the current version of the EMI interface supported by the device.


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
 

 

