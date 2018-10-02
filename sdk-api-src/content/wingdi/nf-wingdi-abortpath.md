---
UID: NF:wingdi.AbortPath
title: AbortPath function
author: windows-sdk-content
description: The AbortPath function closes and discards any paths in the specified device context.
old-location: gdi\abortpath.htm
tech.root: gdi
ms.assetid: 49299a11-910b-40e0-b02e-80a244cfc978
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AbortPath, AbortPath function [Windows GDI], _win32_AbortPath, gdi.abortpath, wingdi/AbortPath
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
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
 - AbortPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AbortPath function


## -description


The <b>AbortPath</b> function closes and discards any paths in the specified device context.


## -parameters




### -param hdc [in]

Handle to the device context from which a path will be discarded.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



If there is an open path bracket in the given device context, the path bracket is closed and the path is discarded. If there is a closed path in the device context, the path is discarded.




## -see-also




<a href="https://msdn.microsoft.com/88be3405-a420-4eb1-935b-099dc3067530">BeginPath</a>



<a href="https://msdn.microsoft.com/0b4daf81-d1d6-45c1-b081-855b7cd8527a">EndPath</a>



<a href="https://msdn.microsoft.com/68390601-1542-41dc-bea0-78f6c3318806">Path Functions</a>



<a href="https://msdn.microsoft.com/fbbd3ea0-9b35-4aaf-8498-187957e29cf0">Paths Overview</a>
 

 

