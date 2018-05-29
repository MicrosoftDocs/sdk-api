---
UID: NF:winddi.DrvSetPixelFormat
title: DrvSetPixelFormat function
author: windows-sdk-content
description: The DrvSetPixelFormat function sets the pixel format of a window.
old-location: display\drvsetpixelformat.htm
old-project: display
ms.assetid: b2211639-13ae-455c-97ef-8145318af591
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: DrvSetPixelFormat, DrvSetPixelFormat function [Display Devices], ddifncs_095cf66c-832a-49c2-9bf2-f97ef74665b2.xml, display.drvsetpixelformat, winddi/DrvSetPixelFormat
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
-	DrvSetPixelFormat
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DrvSetPixelFormat function


## -description


The <b>DrvSetPixelFormat</b> function sets the pixel format of a window.


## -parameters




### -param pso

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a> structure with which the window is associated.


### -param iPixelFormat

Index that specifies the device format to which the pixel format is to be set. The pixel formats that a device supports are identified by positive one-based integer indices starting at 1.


### -param hwnd

Handle to the window whose pixel format is to be set.


## -returns



The return value is <b>TRUE</b> if the function is successful. Otherwise, it is <b>FALSE</b>, and an error code is logged.




## -remarks



Setting the pixel format more than once can result in complications for Window Manager and for multithreaded applications. Consequently, the pixel format of a window can be set only once and must remain unchanged.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556190">DrvDescribePixelFormat</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a>
 

 

