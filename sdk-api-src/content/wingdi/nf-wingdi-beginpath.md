---
UID: NF:wingdi.BeginPath
title: BeginPath function
author: windows-sdk-content
description: The BeginPath function opens a path bracket in the specified device context.
old-location: gdi\beginpath.htm
tech.root: gdi
ms.assetid: 88be3405-a420-4eb1-935b-099dc3067530
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: BeginPath, BeginPath function [Windows GDI], _win32_BeginPath, gdi.beginpath, wingdi/BeginPath
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
 - BeginPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BeginPath function


## -description


The <b>BeginPath</b> function opens a path bracket in the specified device context.


## -parameters




### -param hdc [in]

A handle to the device context.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



After a path bracket is open, an application can begin calling GDI drawing functions to define the points that lie in the path. An application can close an open path bracket by calling the <a href="https://msdn.microsoft.com/0b4daf81-d1d6-45c1-b081-855b7cd8527a">EndPath</a> function.

When an application calls <b>BeginPath</b> for a device context, any previous paths are discarded from that device context. The following list shows which drawing functions can be used.

<ul>
<li>
<a href="https://msdn.microsoft.com/65c38da1-ab7d-4e80-83e3-ba1db66f8fd9">AngleArc</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c15a2173-0fad-4a8a-b0f9-cd39fe4e7bac">Arc</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5e358a14-9f39-4267-9a44-c8bf05b5dfbb">ArcTo</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d6752c47-96a5-4fac-a1bb-0611a91f03f9">Chord</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2532227c-35c9-4a46-b4eb-4a156ef28219">CloseFigure</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9bec59dd-6bcb-498e-9ed2-ac641ecd7fa5">Ellipse</a>
</li>
<li>
<a href="https://msdn.microsoft.com/74f8fcb8-8ad4-47f2-a330-fa56713bdb37">ExtTextOut</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a31b3a9a-110f-4cdf-89d9-19937a2e40b4">LineTo</a>
</li>
<li>
<a href="https://msdn.microsoft.com/af11eeb7-4036-4a90-8685-9b5719f79e01">MoveToEx</a>
</li>
<li>
<a href="https://msdn.microsoft.com/86daa936-b483-4432-aa32-0b9328ff76f9">Pie</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d1622574-c65e-4265-9a17-22bb4d2cae0e">PolyBezier</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0c8d6d6d-d0a3-4188-91ad-934e6f054862">PolyBezierTo</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5fd3f285-dcf3-4cd0-915a-236ba7902353">PolyDraw</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2f958b91-039a-4e02-b727-be142bb18b06">Polygon</a>
</li>
<li>
<a href="https://msdn.microsoft.com/55481dd0-3db7-4131-b383-4d0036943e60">Polyline</a>
</li>
<li>
<a href="https://msdn.microsoft.com/76020742-b651-4244-82c3-13034573c306">PolylineTo</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ac0a2802-c8b0-4cd7-9521-5b179f2c70b9">PolyPolygon</a>
</li>
<li>
<a href="https://msdn.microsoft.com/71a9273f-321b-4efb-ac73-5979f8151d05">PolyPolyline</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ed6b9824-1edc-4510-b9da-a4287845aa83">Rectangle</a>
</li>
<li>
<a href="https://msdn.microsoft.com/17808a6a-7bd0-4fd6-81ab-00d5db764b93">RoundRect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0c437ff8-3893-4dc3-827b-fa9ce4bcd7e6">TextOut</a>
</li>
</ul>

#### Examples

For an example, see <a href="https://msdn.microsoft.com/3eb5781b-972b-49a4-94db-9abda96fb195">Using Paths</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0b4daf81-d1d6-45c1-b081-855b7cd8527a">EndPath</a>



<a href="https://msdn.microsoft.com/a80b299a-c3f9-411b-9936-33d32fc71853">FillPath</a>



<a href="https://msdn.microsoft.com/68390601-1542-41dc-bea0-78f6c3318806">Path Functions</a>



<a href="https://msdn.microsoft.com/9fe31925-3d5d-42e5-aa9b-405610f13de4">PathToRegion</a>



<a href="https://msdn.microsoft.com/fbbd3ea0-9b35-4aaf-8498-187957e29cf0">Paths Overview</a>



<a href="https://msdn.microsoft.com/c5102e1b-ba33-4cce-a4e5-93cf10c1c0bb">SelectClipPath</a>



<a href="https://msdn.microsoft.com/936af9e5-707d-4d43-9035-e8239e3759a2">StrokeAndFillPath</a>



<a href="https://msdn.microsoft.com/5a9f1509-0a69-4db8-8d74-9bf360aca64d">StrokePath</a>



<a href="https://msdn.microsoft.com/c994bd1b-c5e8-46e6-a6a6-59e2d9106d75">WidenPath</a>
 

 

