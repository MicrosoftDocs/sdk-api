---
UID: NF:wingdi.EndPath
title: EndPath function (wingdi.h)
author: windows-sdk-content
description: The EndPath function closes a path bracket and selects the path defined by the bracket into the specified device context.
old-location: gdi\endpath.htm
tech.root: gdi
ms.assetid: 0b4daf81-d1d6-45c1-b081-855b7cd8527a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EndPath, EndPath function [Windows GDI], _win32_EndPath, gdi.endpath, wingdi/EndPath
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
 - Ext-MS-Win-GDI-Path-l1-1-0.dll
 - GDI32Full.dll
api_name:
 - EndPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EndPath function


## -description


The <b>EndPath</b> function closes a path bracket and selects the path defined by the bracket into the specified device context.


## -parameters




### -param hdc [in]

A handle to the device context into which the new path is selected.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/88be3405-a420-4eb1-935b-099dc3067530">BeginPath</a>



<a href="https://msdn.microsoft.com/68390601-1542-41dc-bea0-78f6c3318806">Path Functions</a>



<a href="https://msdn.microsoft.com/fbbd3ea0-9b35-4aaf-8498-187957e29cf0">Paths Overview</a>
 

 

