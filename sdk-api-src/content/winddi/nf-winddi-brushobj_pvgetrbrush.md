---
UID: NF:winddi.BRUSHOBJ_pvGetRbrush
title: BRUSHOBJ_pvGetRbrush function
author: windows-sdk-content
description: The BRUSHOBJ_pvGetRbrush function retrieves a pointer to the driver's realization of a specified brush.
old-location: display\brushobj_pvgetrbrush.htm
old-project: display
ms.assetid: 3f3e5acb-f984-4571-9555-f6b383ddb6a7
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: BRUSHOBJ_pvGetRbrush, BRUSHOBJ_pvGetRbrush function [Display Devices], display.brushobj_pvgetrbrush, gdifncs_a19def34-749c-4e98-b03e-1b35f4e1f761.xml, winddi/BRUSHOBJ_pvGetRbrush
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
 - BRUSHOBJ_pvGetRbrush
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# BRUSHOBJ_pvGetRbrush function


## -description


The <b>BRUSHOBJ_pvGetRbrush</b> function retrieves a pointer to the driver's realization of a specified brush.


## -parameters




### -param pbo

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff538261">BRUSHOBJ</a> structure whose realization is requested.


## -returns



The return value is a pointer to the realized brush if the function is successful. If the brush cannot be realized, the return value is null and an error code is logged.




## -remarks



<b>BRUSHOBJ_pvGetRbrush</b> is called when the brush is a pattern brush that has not yet been realized; that is, it is called when the <b>iSolidColor</b> member of the BRUSHOBJ structure is 0xFFFFFFFF and the <b>pvRbrush</b> member is null.

If the brush has not been realized when <b>BRUSHOBJ_pvGetRbrush</b> is called, GDI calls the driver-supplied <a href="https://msdn.microsoft.com/library/windows/hardware/ff556273">DrvRealizeBrush</a> function to obtain the driver's realization of the brush. As an acceleration, GDI caches this realization in the <b>pvRbrush</b> member of the BRUSHOBJ structure. Then, when an application reuses this brush for another drawing operation, the driver doesn't have to call <b>BRUSHOBJ_pvGetRbrush</b> again.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538261">BRUSHOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538263">BRUSHOBJ_pvAllocRbrush</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556273">DrvRealizeBrush</a>
 

 

