---
UID: NF:winddi.BRUSHOBJ_ulGetBrushColor
title: BRUSHOBJ_ulGetBrushColor function
author: windows-sdk-content
description: The BRUSHOBJ_ulGetBrushColor function returns the RGB color of the specified solid brush.
old-location: display\brushobj_ulgetbrushcolor.htm
old-project: display
ms.assetid: 815844d7-930f-46c3-9403-c61cb2c8a992
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: BRUSHOBJ_ulGetBrushColor, BRUSHOBJ_ulGetBrushColor function [Display Devices], display.brushobj_ulgetbrushcolor, gdifncs_d103f229-9c90-4dbc-ba0b-e909a8371cd8.xml, winddi/BRUSHOBJ_ulGetBrushColor
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
-	BRUSHOBJ_ulGetBrushColor
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# BRUSHOBJ_ulGetBrushColor function


## -description


The <b>BRUSHOBJ_ulGetBrushColor</b> function returns the RGB color of the specified solid brush.


## -parameters




### -param pbo

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff538261">BRUSHOBJ</a> structure whose color is being queried.


## -returns



<b>BRUSHOBJ_ulGetBrushColor</b> returns the RGB color of a solid brush. If the specified brush is not solid, this function returns -1.




## -remarks



The color stored in the <b>iSolidColor</b> member of the BRUSHOBJ structure is an index value that has been translated to the target surface's palette. <b>BRUSHOBJ_ulGetBrushColor</b> allows the driver to query the original RGB color value of <b>iSolidColor</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538261">BRUSHOBJ</a>
 

 

