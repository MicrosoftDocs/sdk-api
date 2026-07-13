---
UID: NS:setupapi._SP_DEVICE_INTERFACE_DETAIL_DATA_A
title: SP_DEVICE_INTERFACE_DETAIL_DATA_A (setupapi.h)
description: An SP_DEVICE_INTERFACE_DETAIL_DATA structure contains the path for a device interface. (ANSI)
helpviewer_keywords: ["*PSP_DEVICE_INTERFACE_DETAIL_DATA_A","PSP_DEVICE_INTERFACE_DETAIL_DATA","PSP_DEVICE_INTERFACE_DETAIL_DATA structure pointer [Device and Driver Installation]","SP_DEVICE_INTERFACE_DETAIL_DATA","SP_DEVICE_INTERFACE_DETAIL_DATA structure [Device and Driver Installation]","SP_DEVICE_INTERFACE_DETAIL_DATA_A","SP_INTERFACE_DEVICE_DETAIL_DATA","SP_INTERFACE_DEVICE_DETAIL_DATA_A","devinst.sp_device_interface_detail_data","di-struct_fbf4856e-f570-4024-b4eb-6ac7555d65ca.xml","setupapi/PSP_DEVICE_INTERFACE_DETAIL_DATA","setupapi/SP_DEVICE_INTERFACE_DETAIL_DATA"]
old-location: devinst\sp_device_interface_detail_data.htm
tech.root: devinst
ms.assetid: 9dd44297-6e51-425d-a355-f2ea78757bf7
ms.date: 12/05/2018
ms.keywords: '*PSP_DEVICE_INTERFACE_DETAIL_DATA_A, PSP_DEVICE_INTERFACE_DETAIL_DATA, PSP_DEVICE_INTERFACE_DETAIL_DATA structure pointer [Device and Driver Installation], SP_DEVICE_INTERFACE_DETAIL_DATA, SP_DEVICE_INTERFACE_DETAIL_DATA structure [Device and Driver Installation], SP_DEVICE_INTERFACE_DETAIL_DATA_A, SP_INTERFACE_DEVICE_DETAIL_DATA, SP_INTERFACE_DEVICE_DETAIL_DATA_A, devinst.sp_device_interface_detail_data, di-struct_fbf4856e-f570-4024-b4eb-6ac7555d65ca.xml, setupapi/PSP_DEVICE_INTERFACE_DETAIL_DATA, setupapi/SP_DEVICE_INTERFACE_DETAIL_DATA'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SP_DEVICE_INTERFACE_DETAIL_DATA_A, *PSP_DEVICE_INTERFACE_DETAIL_DATA_A
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SP_DEVICE_INTERFACE_DETAIL_DATA_A
 - setupapi/_SP_DEVICE_INTERFACE_DETAIL_DATA_A
 - PSP_DEVICE_INTERFACE_DETAIL_DATA_A
 - setupapi/PSP_DEVICE_INTERFACE_DETAIL_DATA_A
 - SP_DEVICE_INTERFACE_DETAIL_DATA_A
 - setupapi/SP_DEVICE_INTERFACE_DETAIL_DATA_A
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - setupapi.h
api_name:
 - SP_DEVICE_INTERFACE_DETAIL_DATA
 - sp_device_interface_detail_data_a
---

# SP_DEVICE_INTERFACE_DETAIL_DATA_A structure


## -description

An SP_DEVICE_INTERFACE_DETAIL_DATA structure contains the path for a device interface.

## -struct-fields

### -field cbSize

The size, in bytes, of the SP_DEVICE_INTERFACE_DETAIL_DATA structure. For more information, see the following Remarks section.

### -field DevicePath

A NULL-terminated string that contains the device interface path. This path can be passed to Win32 functions such as <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>.

## -remarks

An SP_DEVICE_INTERFACE_DETAIL_DATA structure identifies the path for a device interface in a device information set.

<b>SetupDi</b><i>Xxx</i> functions that take an SP_DEVICE_INTERFACE_DETAIL_DATA structure as a parameter verify that the <b>cbSize</b> member of the supplied structure is equal to the size, in bytes, of the structure. If the <b>cbSize</b> member is not set correctly for an input parameter, the function will fail and set an error code of ERROR_INVALID_PARAMETER. If the <b>cbSize</b> member is not set correctly for an output parameter, the function will fail and set an error code of ERROR_INVALID_USER_BUFFER.





> [!NOTE]
> The setupapi.h header defines SP_DEVICE_INTERFACE_DETAIL_DATA as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceinterfacedetaila">SetupDiGetDeviceInterfaceDetail</a>
