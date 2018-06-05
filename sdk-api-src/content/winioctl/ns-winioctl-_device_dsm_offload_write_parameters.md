---
UID: NS:winioctl._DEVICE_DSM_OFFLOAD_WRITE_PARAMETERS
title: "_DEVICE_DSM_OFFLOAD_WRITE_PARAMETERS"
author: windows-sdk-content
description: Specifies parameters for the offload write operation.
old-location: base\device_dsm_offload_write_parameters.htm
old-project: DevIO
ms.assetid: d0107cae-50c9-46d2-97cd-324030692903
ms.author: windowssdkdev
ms.date: 04/03/2018
ms.keywords: "*PDEVICE_DSM_OFFLOAD_WRITE_PARAMETERS, DEVICE_DSM_OFFLOAD_WRITE_PARAMETERS, DEVICE_DSM_OFFLOAD_WRITE_PARAMETERS structure, PDEVICE_DSM_OFFLOAD_WRITE_PARAMETERS, PDEVICE_DSM_OFFLOAD_WRITE_PARAMETERS structure pointer, _DEVICE_DSM_OFFLOAD_WRITE_PARAMETERS, base.device_dsm_offload_write_parameters, winioctl/DEVICE_DSM_OFFLOAD_WRITE_PARAMETERS, winioctl/PDEVICE_DSM_OFFLOAD_WRITE_PARAMETERS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.typenames: DEVICE_DSM_OFFLOAD_WRITE_PARAMETERS, *PDEVICE_DSM_OFFLOAD_WRITE_PARAMETERS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoCtl.h
api_name:
-	DEVICE_DSM_OFFLOAD_WRITE_PARAMETERS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _DEVICE_DSM_OFFLOAD_WRITE_PARAMETERS structure


## -description


Specifies parameters for the offload write operation. An offload write operation is 
    initiated by specifying <b>DeviceDsmAction_OffloadWrite</b> in the 
    <b>Action</b> member of the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff552527">DEVICE_MANAGE_DATA_SET_ATTRIBUTES</a> 
    structure passed in a 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff560573">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a> 
    control code.


## -struct-fields




### -field Flags

Set to 0.


### -field Reserved

Reserved.


### -field TokenOffset

The starting offset to copy from the range bound to the token


### -field Token


<a href="https://msdn.microsoft.com/library/windows/hardware/hh451469">STORAGE_OFFLOAD_TOKEN</a> structure containing 
      the token returned from the offload read operation.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552527">DEVICE_MANAGE_DATA_SET_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/85ebbdca-94a0-4467-8d15-ee3a850e1cd9">Device Management Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff560573">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh451469">STORAGE_OFFLOAD_TOKEN</a>
 

 

