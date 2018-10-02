---
UID: NF:winddi.STROBJ_dwGetCodePage
title: STROBJ_dwGetCodePage function
author: windows-sdk-content
description: The STROBJ_dwGetCodePage function returns the code page associated with the specified STROBJ structure.
old-location: display\strobj_dwgetcodepage.htm
tech.root: Display
ms.assetid: b28e5854-1ac0-4b76-87a9-ec943228e2ed
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: STROBJ_dwGetCodePage, STROBJ_dwGetCodePage function [Display Devices], display.strobj_dwgetcodepage, gdifncs_e446480e-8516-4138-8121-1c9665fc22d9.xml, winddi/STROBJ_dwGetCodePage
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
 - STROBJ_dwGetCodePage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# STROBJ_dwGetCodePage function


## -description


The <b>STROBJ_dwGetCodePage</b> function returns the code page associated with the specified STROBJ structure.


## -parameters




### -param pstro

Pointer to a <a href="https://msdn.microsoft.com/efe53cb8-39b9-4931-bac2-9c61efd9d457">STROBJ</a> structure with which the code page is associated.


## -returns



<b>STROBJ_dwGetCodePage</b> returns a DWORD value that identifies the code page associated with the font used in the text output call at the Win32 API level.




## -see-also




<a href="https://msdn.microsoft.com/efe53cb8-39b9-4931-bac2-9c61efd9d457">STROBJ</a>
 

 

