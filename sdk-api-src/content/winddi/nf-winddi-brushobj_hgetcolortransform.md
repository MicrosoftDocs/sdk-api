---
UID: NF:winddi.BRUSHOBJ_hGetColorTransform
title: BRUSHOBJ_hGetColorTransform function
author: windows-sdk-content
description: The BRUSHOBJ_hGetColorTransform function retrieves the color transform for the specified brush.
old-location: display\brushobj_hgetcolortransform.htm
old-project: display
ms.assetid: a62544e5-f4b6-4544-8ec1-5a03f8bd3306
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: BRUSHOBJ_hGetColorTransform, BRUSHOBJ_hGetColorTransform function [Display Devices], display.brushobj_hgetcolortransform, gdifncs_eeb575c7-44b8-4af6-ab2d-6bb1afc3af32.xml, winddi/BRUSHOBJ_hGetColorTransform
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
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Win32k.sys
api_name:
-	BRUSHOBJ_hGetColorTransform
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# BRUSHOBJ_hGetColorTransform function


## -description


The <b>BRUSHOBJ_hGetColorTransform</b> function retrieves the color transform for the specified brush.


## -parameters




### -param pbo

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff538261">BRUSHOBJ</a> structure whose color transform is being queried. The color transform was created in a prior call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff556239">DrvIcmCreateColorTransform</a>.


## -returns



<b>BRUSHOBJ_hGetColorTransform</b> returns a handle to the color transform for the specified BRUSHOBJ structure upon success. Otherwise, it returns <b>NULL</b>.




## -remarks



<b>BRUSHOBJ_hGetColorTransform</b> returns <b>NULL</b> when ICM is disabled.

The color transform for a translation object is obtained by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff570639">XLATEOBJ_hGetColorTransform</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538261">BRUSHOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556239">DrvIcmCreateColorTransform</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570639">XLATEOBJ_hGetColorTransform</a>
 

 

