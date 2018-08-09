---
UID: NF:winddi.PATHOBJ_bMoveTo
title: PATHOBJ_bMoveTo function
author: windows-sdk-content
description: The PATHOBJ_bMoveTo function sets the current position in a given path.
old-location: display\pathobj_bmoveto.htm
old-project: display
ms.assetid: b734ce8f-7e7e-4c13-a614-cb6b0dc19ead
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: PATHOBJ_bMoveTo, PATHOBJ_bMoveTo function [Display Devices], display.pathobj_bmoveto, gdifncs_a6917397-5fcb-41fd-8f5a-f6af95ee7bb2.xml, winddi/PATHOBJ_bMoveTo
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
 - PATHOBJ_bMoveTo
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# PATHOBJ_bMoveTo function


## -description


The <b>PATHOBJ_bMoveTo</b> function sets the current position in a given path.


## -parameters




### -param ppo

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff568849">PATHOBJ</a> structure created by the driver.


### -param ptfx

Pointer to a POINTFIX structure that specifies the new position. For a description of this data type, see <a href="https://msdn.microsoft.com/2054aa16-6d86-4db3-8b16-4570b0374e23">GDI Data Types</a>.


## -returns



The return value is <b>TRUE</b> if the function is successful. Otherwise, it is <b>FALSE</b>, and an error code is logged.




## -remarks



This function should only be called with PATHOBJ structures created by <a href="https://msdn.microsoft.com/library/windows/hardware/ff564755">EngCreatePath</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564755">EngCreatePath</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568849">PATHOBJ</a>
 

 

