---
UID: NF:wingdi.GetMetaRgn
title: GetMetaRgn function
author: windows-sdk-content
description: The GetMetaRgn function retrieves the current metaregion for the specified device context.
old-location: gdi\getmetargn.htm
old-project: gdi
ms.assetid: 9c2741cf-30e4-4100-bae9-ad99a7ae37f1
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetMetaRgn, GetMetaRgn function [Windows GDI], _win32_GetMetaRgn, gdi.getmetargn, wingdi/GetMetaRgn
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - GetMetaRgn
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetMetaRgn function


## -description


The <b>GetMetaRgn</b> function retrieves the current metaregion for the specified device context.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param hrgn [in]

A handle to an existing region before the function is called. After the function returns, this parameter is a handle to a copy of the current metaregion.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



If the function succeeds, <i>hrgn</i> is a handle to a copy of the current metaregion. Subsequent changes to this copy will not affect the current metaregion.

The current clipping region of a device context is defined by the intersection of its clipping region and its metaregion.




## -see-also




<a href="https://msdn.microsoft.com/de9e5786-63d8-47be-8522-e96d7c0f8634">Clipping Functions</a>



<a href="https://msdn.microsoft.com/9e966369-9988-4bfa-af37-b1bbb3488880">Clipping Overview</a>



<a href="https://msdn.microsoft.com/79f5dc01-bdec-4844-be94-1f9cf5bfd712">SetMetaRgn</a>
 

 

