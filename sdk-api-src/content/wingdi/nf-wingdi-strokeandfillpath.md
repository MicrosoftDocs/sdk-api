---
UID: NF:wingdi.StrokeAndFillPath
title: StrokeAndFillPath function
author: windows-sdk-content
description: The StrokeAndFillPath function closes any open figures in a path, strokes the outline of the path by using the current pen, and fills its interior by using the current brush.
old-location: gdi\strokeandfillpath.htm
tech.root: gdi
ms.assetid: 936af9e5-707d-4d43-9035-e8239e3759a2
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: StrokeAndFillPath, StrokeAndFillPath function [Windows GDI], _win32_StrokeAndFillPath, gdi.strokeandfillpath, wingdi/StrokeAndFillPath
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
 - StrokeAndFillPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# StrokeAndFillPath function


## -description


The <b>StrokeAndFillPath</b> function closes any open figures in a path, strokes the outline of the path by using the current pen, and fills its interior by using the current brush.


## -parameters




### -param hdc [in]

A handle to the device context.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The device context identified by the <i>hdc</i> parameter must contain a closed path.

The <b>StrokeAndFillPath</b> function has the same effect as closing all the open figures in the path, and stroking and filling the path separately, except that the filled region will not overlap the stroked region even if the pen is wide.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/788d3bc2-1010-436c-a95f-6fe55daac88e">Drawing a Pie Chart</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/88be3405-a420-4eb1-935b-099dc3067530">BeginPath</a>



<a href="https://msdn.microsoft.com/a80b299a-c3f9-411b-9936-33d32fc71853">FillPath</a>



<a href="https://msdn.microsoft.com/68390601-1542-41dc-bea0-78f6c3318806">Path Functions</a>



<a href="https://msdn.microsoft.com/fbbd3ea0-9b35-4aaf-8498-187957e29cf0">Paths Overview</a>



<a href="https://msdn.microsoft.com/233926c4-2658-405d-89b6-05ece844623d">SetPolyFillMode</a>



<a href="https://msdn.microsoft.com/5a9f1509-0a69-4db8-8d74-9bf360aca64d">StrokePath</a>
 

 

