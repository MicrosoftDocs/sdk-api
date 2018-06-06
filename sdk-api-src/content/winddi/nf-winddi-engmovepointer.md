---
UID: NF:winddi.EngMovePointer
title: EngMovePointer function
author: windows-sdk-content
description: The EngMovePointer function moves the engine-managed pointer on the device.
old-location: display\engmovepointer.htm
old-project: display
ms.assetid: 6f427839-034e-46c3-a3b0-703a003af1e4
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: EngMovePointer, EngMovePointer function [Display Devices], display.engmovepointer, gdifncs_2499e137-74e8-4624-8595-65d4fb489973.xml, winddi/EngMovePointer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngMovePointer
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngMovePointer function


## -description


The <b>EngMovePointer</b> function moves the engine-managed pointer on the device.


## -parameters




### -param pso [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a> structure that describes the display device surface on which the pointer is to be moved.


### -param x [in]

Specify the x-coordinate on the display where the hot spot of the pointer should be positioned.

A negative <i>x</i> value indicates that the pointer should be removed from the display because drawing is about to occur at its present location. If the pointer has been removed from the display and the <i>x</i> value is nonnegative, the pointer should be restored.


### -param y [in]

Specify the y-coordinate on the display where the hot spot of the pointer should be positioned.


### -param prcl [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569236">RECTL</a> structure defining an area that bounds all pixels affected by the pointer on the display. The driver should pass the <i>prcl</i> parameter received by its <a href="https://msdn.microsoft.com/library/windows/hardware/ff556248">DrvMovePointer</a> function. GDI will not draw in this rectangle without first removing the pointer from the screen. This parameter can be <b>NULL</b>.


## -returns



None




## -remarks



<b>EngMovePointer</b> must not be called while any thread is drawing in the display driver.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552835">DEVINFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556248">DrvMovePointer</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565017">EngSetPointerShape</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a>
 

 

