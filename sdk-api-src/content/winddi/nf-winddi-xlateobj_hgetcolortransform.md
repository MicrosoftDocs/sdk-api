---
UID: NF:winddi.XLATEOBJ_hGetColorTransform
title: XLATEOBJ_hGetColorTransform function
author: windows-sdk-content
description: The XLATEOBJ_hGetColorTransform function returns the color transform for the specified translation object.
old-location: display\xlateobj_hgetcolortransform.htm
old-project: display
ms.assetid: dd109ae8-c368-4e8a-bf25-405ed96484e3
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: XLATEOBJ_hGetColorTransform, XLATEOBJ_hGetColorTransform function [Display Devices], display.xlateobj_hgetcolortransform, gdifncs_6df99fb8-f6ad-4fe8-a140-c004700b9d33.xml, winddi/XLATEOBJ_hGetColorTransform
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
 - XLATEOBJ_hGetColorTransform
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# XLATEOBJ_hGetColorTransform function


## -description


The <b>XLATEOBJ_hGetColorTransform</b> function returns the color transform for the specified translation object.


## -parameters




### -param pxlo

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff570634">XLATEOBJ</a> structure whose color transform is being queried. The color transform was created in a prior call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff556239">DrvIcmCreateColorTransform</a>.


## -returns



<b>XLATEOBJ_hGetColorTransform</b> returns a handle to the color transform for the specified XLATEOBJ upon success. Otherwise, it returns <b>NULL</b>.




## -remarks



<b>XLATEOBJ_hGetColorTransform</b> returns <b>NULL</b> when it is called in host ICM context or when ICM is disabled.

The color transform for a brush is obtained by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff538262">BRUSHOBJ_hGetColorTransform</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538262">BRUSHOBJ_hGetColorTransform</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556239">DrvIcmCreateColorTransform</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570634">XLATEOBJ</a>
 

 

