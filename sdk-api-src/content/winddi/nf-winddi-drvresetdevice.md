---
UID: NF:winddi.DrvResetDevice
title: DrvResetDevice function
author: windows-sdk-content
description: The DrvResetDevice function resets a device that is inoperable or unresponsive.
old-location: display\drvresetdevice.htm
old-project: display
ms.assetid: 2078cefe-3b66-455b-a4cc-144d643f74e7
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: DrvResetDevice, DrvResetDevice function [Display Devices], ddifncs_ba6f8e5e-bd3a-4666-ab2c-d9bb56495712.xml, display.drvresetdevice, winddi/DrvResetDevice
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Desktop
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
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winddi.h
api_name:
-	DrvResetDevice
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DrvResetDevice function


## -description


The <b>DrvResetDevice</b> function resets a device that is inoperable or unresponsive.


## -parameters




### -param dhpdev

Handle to the physical device's PDEV that describes the physical device that has stopped. This is the value returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>.


### -param Reserved

Is reserved and must be set to <b>NULL</b>.


## -returns



<b>DrvResetDevice</b> should return one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRD_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The device did not recover from the error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRD_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The device is currently in working order.

</td>
</tr>
</table>
 




## -remarks



This function is available in Windows XP and later.

<b>DrvResetDevice</b> is usually called in response to <a href="https://msdn.microsoft.com/library/windows/hardware/ff564958">EngHangNotification</a>. A driver should take any steps necessary to restore the device to working order, and should do so with no data loss or as little as possible.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564958">EngHangNotification</a>
 

 

