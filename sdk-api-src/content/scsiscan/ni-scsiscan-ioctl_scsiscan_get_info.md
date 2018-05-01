---
UID: NI:scsiscan.IOCTL_SCSISCAN_GET_INFO
title: IOCTL_SCSISCAN_GET_INFO
author: windows-driver-content
description: The IOCTL_SCSISCAN_GET_INFO I/O control code returns device information.
old-location: image\ioctl_scsiscan_get_info.htm
old-project: image
ms.assetid: 48045e29-5982-44e6-b9a7-3b000e5cf338
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IOCTL_SCSISCAN_GET_INFO, IOCTL_SCSISCAN_GET_INFO control code [Imaging Devices], image.ioctl_scsiscan_get_info, scsiscan/IOCTL_SCSISCAN_GET_INFO, stifnc_5897897c-6c10-42cd-9301-d5b5f54675fd.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: scsiscan.h
req.include-header: Scsiscan.h
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
req.typenames: SCHEDULE_HEADER, *PSCHEDULE_HEADER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	scsiscan.h
api_name:
-	IOCTL_SCSISCAN_GET_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOCTL_SCSISCAN_GET_INFO IOCTL


## -description


The <b>IOCTL_SCSISCAN_GET_INFO</b> I/O control code returns device information.


## -ioctlparameters




### -input-buffer

Set to NULL.


### -input-buffer-length

Set to 0.


### -output-buffer

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff547981">SCSISCAN_INFO</a> structure.


### -output-buffer-length

Size of output buffer.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

<b>Irp-&gt;IoStatus.Status</b> is set to STATUS_SUCCESS if the request is successful. Otherwise, <b>Status</b> to the appropriate error condition as a <a href="https://msdn.microsoft.com/7792201b-63bb-4db5-803d-2af02893d505">NTSTATUS</a> code. 


## -remarks



When the DeviceloControl function is called with the <b>IOCTL_SCSISCAN_GET_INFO</b> I/O control code, the caller must specify the address of a SCSISCAN_INFO structure as the function's lpOutbuffer parameter. The kernel-mode driver fills in the structure.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff542894">Creating IOCTL Requests in Drivers</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548651">WdfIoTargetSendInternalIoctlOthersSynchronously</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548656">WdfIoTargetSendInternalIoctlSynchronously</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548660">WdfIoTargetSendIoctlSynchronously</a>
 

 

