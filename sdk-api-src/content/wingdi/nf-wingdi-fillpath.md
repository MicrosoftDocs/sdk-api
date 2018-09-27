---
UID: NF:wingdi.FillPath
title: FillPath function
author: windows-sdk-content
description: The FillPath function closes any open figures in the current path and fills the path's interior by using the current brush and polygon-filling mode.
old-location: gdi\fillpath.htm
tech.root: gdi
ms.assetid: a80b299a-c3f9-411b-9936-33d32fc71853
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: FillPath, FillPath function [Windows GDI], _win32_FillPath, gdi.fillpath, wingdi/FillPath
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
 - Ext-MS-Win-GDI-Path-l1-1-0.dll
 - GDI32Full.dll
api_name:
 - FillPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FillPath function


## -description


The <b>FillPath</b> function closes any open figures in the current path and fills the path's interior by using the current brush and polygon-filling mode.


## -parameters




### -param hdc [in]

A handle to a device context that contains a valid path.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



After its interior is filled, the path is discarded from the DC identified by the <i>hdc</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/88be3405-a420-4eb1-935b-099dc3067530">BeginPath</a>



<a href="https://msdn.microsoft.com/68390601-1542-41dc-bea0-78f6c3318806">Path Functions</a>



<a href="https://msdn.microsoft.com/fbbd3ea0-9b35-4aaf-8498-187957e29cf0">Paths Overview</a>



<a href="https://msdn.microsoft.com/233926c4-2658-405d-89b6-05ece844623d">SetPolyFillMode</a>



<a href="https://msdn.microsoft.com/936af9e5-707d-4d43-9035-e8239e3759a2">StrokeAndFillPath</a>



<a href="https://msdn.microsoft.com/5a9f1509-0a69-4db8-8d74-9bf360aca64d">StrokePath</a>
 

 

