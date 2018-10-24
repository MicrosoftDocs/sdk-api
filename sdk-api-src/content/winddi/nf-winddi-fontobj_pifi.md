---
UID: NF:winddi.FONTOBJ_pifi
title: FONTOBJ_pifi function
author: windows-sdk-content
description: The FONTOBJ_pifi function retrieves the pointer to the IFIMETRICS structure associated with a specified font.
old-location: display\fontobj_pifi.htm
tech.root: display
ms.assetid: 797341c8-7346-477a-9c7c-b6abbeaac4b2
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: FONTOBJ_pifi, FONTOBJ_pifi function [Display Devices], display.fontobj_pifi, gdifncs_702d11ac-850f-4e4d-aefa-1ccf404edb56.xml, winddi/FONTOBJ_pifi
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - FONTOBJ_pifi
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FONTOBJ_pifi function


## -description


The <b>FONTOBJ_pifi</b> function retrieves the pointer to the <a href="https://msdn.microsoft.com/fd2606ed-ec61-430a-aaad-38a4c3a207b6">IFIMETRICS</a> structure associated with a specified font.


## -parameters




### -param pfo

Pointer to the <a href="https://msdn.microsoft.com/09af2006-51f1-433e-9227-3c99b9860e75">FONTOBJ</a> structure for which the associated IFIMETRICS structure is to be retrieved.


## -returns



The return value is a pointer to the IFIMETRICS structure associated with the specified font if the function is successful. Otherwise, it is <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/09af2006-51f1-433e-9227-3c99b9860e75">FONTOBJ</a>



<a href="https://msdn.microsoft.com/fd2606ed-ec61-430a-aaad-38a4c3a207b6">IFIMETRICS</a>
 

 

