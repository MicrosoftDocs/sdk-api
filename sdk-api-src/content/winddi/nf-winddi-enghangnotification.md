---
UID: NF:winddi.EngHangNotification
title: EngHangNotification function (winddi.h)
description: The EngHangNotification function notifies the system that a specified device is inoperable or unresponsive.
helpviewer_keywords: ["EngHangNotification","EngHangNotification function [Display Devices]","display.enghangnotification","gdifncs_ca454eea-7e11-4af6-a717-818f52f9fc59.xml","winddi/EngHangNotification"]
old-location: display\enghangnotification.htm
tech.root: display
ms.assetid: 9013bf34-64bd-4621-af40-f979065c8cbd
ms.date: 12/05/2018
ms.keywords: EngHangNotification, EngHangNotification function [Display Devices], display.enghangnotification, gdifncs_ca454eea-7e11-4af6-a717-818f52f9fc59.xml, winddi/EngHangNotification
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: This function is available in Windows XP and later.
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
 - EngHangNotification
 - winddi/EngHangNotification
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
 - EngHangNotification
---

# EngHangNotification function


## -description

The <b>EngHangNotification</b> function notifies the system that a specified device is inoperable or unresponsive.

## -parameters

### -param hdev

Handle to the physical device that has stopped. This parameter is the GDI handle received by the driver's <a href="/windows/desktop/api/winddi/nf-winddi-drvcompletepdev">DrvCompletePDEV</a> entry point.

### -param Reserved

Is reserved and must be set to <b>NULL</b>.

## -returns

<b>EngHangNotification</b> returns one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>EHN_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The device did not recover from the error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>EHN_RESTORED</b></dt>
</dl>
</td>
<td width="60%">
The device was restored to working order.

</td>
</tr>
</table>

## -remarks

A driver should make this call any time it detects that the hardware is inoperable or unresponsive. If <b>EngHangNotification</b> returns EHN_RESTORED, the driver should retry the operation that detected the inoperable state; otherwise the driver should fail the current call as soon as possible. Any subsequent driver operations that detect a problem should again call <b>EngHangNotification</b>.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvcompletepdev">DrvCompletePDEV</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvresetdevice">DrvResetDevice</a>