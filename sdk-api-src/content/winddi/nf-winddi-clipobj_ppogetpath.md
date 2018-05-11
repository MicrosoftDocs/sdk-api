---
UID: NF:winddi.CLIPOBJ_ppoGetPath
title: CLIPOBJ_ppoGetPath function
author: windows-driver-content
description: The CLIPOBJ_ppoGetPath function creates a PATHOBJ structure that contains the outline of the specified clip region.
old-location: display\clipobj_ppogetpath.htm
old-project: display
ms.assetid: c87d1580-ab24-49a7-b497-87d781be6e5f
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: CLIPOBJ_ppoGetPath, CLIPOBJ_ppoGetPath function [Display Devices], display.clipobj_ppogetpath, gdifncs_576284af-4aef-45be-b10a-2504c8e3451f.xml, winddi/CLIPOBJ_ppoGetPath
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Win32k.sys
api_name:
-	CLIPOBJ_ppoGetPath
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# CLIPOBJ_ppoGetPath function


## -description


The <b>CLIPOBJ_ppoGetPath</b> function creates a <a href="https://msdn.microsoft.com/library/windows/hardware/ff568849">PATHOBJ</a> structure that contains the outline of the specified clip region.


## -parameters




### -param pco [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff539417">CLIPOBJ</a> structure that defines the specified clip region.


## -returns



The return value is a pointer to a PATHOBJ structure if the function is successful. Otherwise, it is <b>NULL</b>, and an error code is logged.




## -remarks



The returned PATHOBJ structure should be deleted using <a href="https://msdn.microsoft.com/library/windows/hardware/ff564811">EngDeletePath</a> when the driver no longer needs it.

A driver for a device that can download a clipping path might prefer this function for defining complex regions.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff539417">CLIPOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564811">EngDeletePath</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568849">PATHOBJ</a>
 

 

