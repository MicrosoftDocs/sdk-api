---
UID: NS:setupapi._SP_DEVICE_INTERFACE_DETAIL_DATA_A
title: "_SP_DEVICE_INTERFACE_DETAIL_DATA_A"
author: windows-sdk-content
description: An SP_DEVICE_INTERFACE_DETAIL_DATA structure contains the path for a device interface.
old-location: devinst\sp_device_interface_detail_data.htm
old-project: devinst
ms.assetid: 9dd44297-6e51-425d-a355-f2ea78757bf7
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*PSP_DEVICE_INTERFACE_DETAIL_DATA_A, PSP_DEVICE_INTERFACE_DETAIL_DATA, PSP_DEVICE_INTERFACE_DETAIL_DATA structure pointer [Device and Driver Installation], SP_DEVICE_INTERFACE_DETAIL_DATA, SP_DEVICE_INTERFACE_DETAIL_DATA structure [Device and Driver Installation], SP_DEVICE_INTERFACE_DETAIL_DATA_A, SP_INTERFACE_DEVICE_DETAIL_DATA, SP_INTERFACE_DEVICE_DETAIL_DATA_A, _SP_DEVICE_INTERFACE_DETAIL_DATA_A, devinst.sp_device_interface_detail_data, di-struct_fbf4856e-f570-4024-b4eb-6ac7555d65ca.xml, setupapi/PSP_DEVICE_INTERFACE_DETAIL_DATA, setupapi/SP_DEVICE_INTERFACE_DETAIL_DATA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: setupapi.h
req.include-header: Setupapi.h
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
req.typenames: SP_DEVICE_INTERFACE_DETAIL_DATA_A, *PSP_DEVICE_INTERFACE_DETAIL_DATA_A
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	setupapi.h
api_name:
-	SP_DEVICE_INTERFACE_DETAIL_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _SP_DEVICE_INTERFACE_DETAIL_DATA_A structure


## -description


An SP_DEVICE_INTERFACE_DETAIL_DATA structure contains the path for a device interface.


## -struct-fields




### -field cbSize

The size, in bytes, of the SP_DEVICE_INTERFACE_DETAIL_DATA structure. For more information, see the following Remarks section.


### -field DevicePath

A NULL-terminated string that contains the device interface path. This path can be passed to Win32 functions such as <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>. 


## -remarks



An SP_DEVICE_INTERFACE_DETAIL_DATA structure identifies the path for a device interface in a device information set.

<b>SetupDi</b><i>Xxx</i> functions that take an SP_DEVICE_INTERFACE_DETAIL_DATA structure as a parameter verify that the <b>cbSize</b> member of the supplied structure is equal to the size, in bytes, of the structure. If the <b>cbSize</b> member is not set correctly for an input parameter, the function will fail and set an error code of ERROR_INVALID_PARAMETER. If the <b>cbSize</b> member is not set correctly for an output parameter, the function will fail and set an error code of ERROR_INVALID_USER_BUFFER.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551120">SetupDiGetDeviceInterfaceDetail</a>
 

 

