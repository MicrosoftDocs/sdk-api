---
UID: NF:winddi.DrvDeleteDeviceBitmap
title: DrvDeleteDeviceBitmap function
author: windows-sdk-content
description: The DrvDeleteDeviceBitmap function deletes a device bitmap created by DrvCreateDeviceBitmap.
old-location: display\drvdeletedevicebitmap.htm
old-project: display
ms.assetid: cb52b133-95c6-4a3d-b8b6-e1628a301542
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: DrvDeleteDeviceBitmap, DrvDeleteDeviceBitmap function [Display Devices], ddifncs_3c8f9ccd-c145-481c-9d31-6a951557527d.xml, display.drvdeletedevicebitmap, winddi/DrvDeleteDeviceBitmap
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvDeleteDeviceBitmap
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DrvDeleteDeviceBitmap function


## -description


The <b>DrvDeleteDeviceBitmap</b> function deletes a device bitmap created by <a href="https://msdn.microsoft.com/library/windows/hardware/ff556185">DrvCreateDeviceBitmap</a>.


## -parameters




### -param dhsurf

Handle to the bitmap to be deleted. This handle identifies the bitmap created by <a href="https://msdn.microsoft.com/library/windows/hardware/ff556185">DrvCreateDeviceBitmap</a>.


## -returns



None




## -remarks



A driver must implement <b>DrvDeleteDeviceBitmap</b> if it supplies <a href="https://msdn.microsoft.com/library/windows/hardware/ff556185">DrvCreateDeviceBitmap</a>.

The driver should free any resources associated with the device bitmap.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556185">DrvCreateDeviceBitmap</a>
 

 

