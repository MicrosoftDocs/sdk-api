---
UID: NF:wingdi.FlattenPath
title: FlattenPath function
author: windows-sdk-content
description: The FlattenPath function transforms any curves in the path that is selected into the current device context (DC), turning each curve into a sequence of lines.
old-location: gdi\flattenpath.htm
tech.root: gdi
ms.assetid: 267b0c9a-25d4-4b04-95d3-6b0856bed022
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FlattenPath, FlattenPath function [Windows GDI], _win32_FlattenPath, gdi.flattenpath, wingdi/FlattenPath
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
 - FlattenPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FlattenPath function


## -description


The <b>FlattenPath</b> function transforms any curves in the path that is selected into the current device context (DC), turning each curve into a sequence of lines.


## -parameters




### -param hdc [in]

A handle to a DC that contains a valid path.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/68390601-1542-41dc-bea0-78f6c3318806">Path Functions</a>



<a href="https://msdn.microsoft.com/fbbd3ea0-9b35-4aaf-8498-187957e29cf0">Paths Overview</a>



<a href="https://msdn.microsoft.com/c994bd1b-c5e8-46e6-a6a6-59e2d9106d75">WidenPath</a>
 

 

