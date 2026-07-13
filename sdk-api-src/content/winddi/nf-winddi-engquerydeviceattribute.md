---
UID: NF:winddi.EngQueryDeviceAttribute
title: EngQueryDeviceAttribute function (winddi.h)
description: The EngQueryDeviceAttribute function allows the driver to query the system about particular attributes of the device.
helpviewer_keywords: ["EngQueryDeviceAttribute","EngQueryDeviceAttribute function [Display Devices]","display.engquerydeviceattribute","gdifncs_1f76b3e8-f265-4959-a7f0-4bc433936be7.xml","winddi/EngQueryDeviceAttribute"]
old-location: display\engquerydeviceattribute.htm
tech.root: display
ms.assetid: 767d0d78-c17f-461b-8ca6-04a00dc456de
ms.date: 12/05/2018
ms.keywords: EngQueryDeviceAttribute, EngQueryDeviceAttribute function [Display Devices], display.engquerydeviceattribute, gdifncs_1f76b3e8-f265-4959-a7f0-4bc433936be7.xml, winddi/EngQueryDeviceAttribute
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
 - EngQueryDeviceAttribute
 - winddi/EngQueryDeviceAttribute
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-full-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngQueryDeviceAttribute
---

# EngQueryDeviceAttribute function


## -description

The <b>EngQueryDeviceAttribute</b> function allows the driver to query the system about particular attributes of the device.

## -parameters

### -param hdev [in]

Handle to the device. This parameter is the GDI handle received by the driver's <a href="/windows/desktop/api/winddi/nf-winddi-drvcompletepdev">DrvCompletePDEV</a> function.

### -param devAttr [in]

Specifies the attribute for which GDI should return information. This parameter must be QDA_ACCELERATION_LEVEL, which queries the driver accelerations that GDI currently allows.

### -param pvIn [in]

Reserved for system use. This parameter is currently ignored by GDI.

### -param ulInSize [in]

Reserved for system use. This parameter is currently ignored by GDI.

### -param pvOut [out]

Pointer to a buffer of <i>ulOutSize</i> bytes in which GDI writes information about the attribute being queried. When <i>devAttr</i> is QDA_ACCELERATION_LEVEL, GDI writes in the buffer a DWORD value from 0 through 5 that indicates the current acceleration level. See <a href="/windows-hardware/drivers/display/display-driver-testing-tools">Display Driver Testing Tools</a> for a description of the acceleration levels.

### -param ulOutSize [out]

Specifies the size, in bytes, of the buffer to which <i>pvOut</i> points.

## -returns

<b>EngQueryDeviceAttribute</b> returns <b>TRUE</b> upon success; otherwise, it returns <b>FALSE</b>.

## -remarks

The video card's acceleration level can be dynamically set through the Display program in Control Panel. <b>EngQueryDeviceAttribute</b> allows the driver to determine the acceleration level currently set.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvnotify">DrvNotify</a>