---
UID: NF:winddi.EngDeviceIoControl
title: EngDeviceIoControl function (winddi.h)
description: The EngDeviceIoControl function sends a control code to the specified video miniport driver, causing the device to perform the specified operation.
helpviewer_keywords: ["EngDeviceIoControl","EngDeviceIoControl function [Display Devices]","display.engdeviceiocontrol","gdifncs_735d205a-99e3-4397-a5ac-31312ac734e7.xml","winddi/EngDeviceIoControl"]
old-location: display\engdeviceiocontrol.htm
tech.root: display
ms.assetid: a38186b6-4b27-4360-8721-49c95dd94806
ms.date: 12/05/2018
ms.keywords: EngDeviceIoControl, EngDeviceIoControl function [Display Devices], display.engdeviceiocontrol, gdifncs_735d205a-99e3-4397-a5ac-31312ac734e7.xml, winddi/EngDeviceIoControl
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EngDeviceIoControl
 - winddi/EngDeviceIoControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-base-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngDeviceIoControl
---

# EngDeviceIoControl function


## -description

The <b>EngDeviceIoControl</b> function sends a control code to the specified video miniport driver, causing the device to perform the specified operation.

## -parameters

### -param hDevice [in]

Handle to the device that is to perform the operation.

### -param dwIoControlCode [in]

Specifies the control code for the operation. The I/O controls are listed and described in full in <a href="/windows-hardware/drivers/ddi/content/index">Video Miniport Driver I/O Control Codes</a>.

### -param lpInBuffer [in, optional]

Pointer to a buffer containing data required to perform the operation. This parameter can be <b>NULL</b> if the control code specifies an operation that does not require input data.

### -param nInBufferSize [in]

Specifies the size, in bytes, of <i>lpInBuffer</i>.

### -param lpOutBuffer [out, optional]

Pointer to a buffer in which the operation's output data is returned. This parameter can be <b>NULL</b> if the control code specifies an operation that does not produce output data.

### -param nOutBufferSize [in]

Specifies the size, in bytes, of <i>lpOutBuffer</i>.

### -param lpBytesReturned [out]

Pointer to a DWORD that specifies the actual size, in bytes, of the data returned in <i>lpOutBuffer</i>.

## -returns

The return value is a 32-bit Win32 API-defined error code.

## -remarks

<b>EngDeviceIoControl</b> is used by a display driver to communicate I/O requests to its corresponding miniport driver. This function provides the only communication channel between a display and video miniport driver.

## -see-also

<a href="/windows-hardware/drivers/ddi/content/video/ns-video-_video_request_packet">VIDEO_REQUEST_PACKET</a>