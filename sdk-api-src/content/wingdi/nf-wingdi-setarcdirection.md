---
UID: NF:wingdi.SetArcDirection
title: SetArcDirection function
author: windows-sdk-content
description: The SetArcDirection sets the drawing direction to be used for arc and rectangle functions.
old-location: gdi\setarcdirection.htm
old-project: gdi
ms.assetid: cec31eb2-cc9d-4384-b973-dd4339b96ed0
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: AD_CLOCKWISE, AD_COUNTERCLOCKWISE, SetArcDirection, SetArcDirection function [Windows GDI], _win32_SetArcDirection, gdi.setarcdirection, wingdi/SetArcDirection
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
 - SetArcDirection
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetArcDirection function


## -description


The <b>SetArcDirection</b> sets the drawing direction to be used for arc and rectangle functions.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param dir

TBD




#### - ArcDirection [in]

The new arc direction. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AD_COUNTERCLOCKWISE"></a><a id="ad_counterclockwise"></a><dl>
<dt><b>AD_COUNTERCLOCKWISE</b></dt>
</dl>
</td>
<td width="60%">
Figures drawn counterclockwise.

</td>
</tr>
<tr>
<td width="40%"><a id="AD_CLOCKWISE"></a><a id="ad_clockwise"></a><dl>
<dt><b>AD_CLOCKWISE</b></dt>
</dl>
</td>
<td width="60%">
Figures drawn clockwise.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value specifies the old arc direction.

If the function fails, the return value is zero.




## -remarks



The default direction is counterclockwise.

The <b>SetArcDirection</b> function specifies the direction in which the following functions draw:

<ul>
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
<a href="https://msdn.microsoft.com/9bec59dd-6bcb-498e-9ed2-ac641ecd7fa5">Ellipse</a>
</li>
<li>
<a href="https://msdn.microsoft.com/86daa936-b483-4432-aa32-0b9328ff76f9">Pie</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ed6b9824-1edc-4510-b9da-a4287845aa83">Rectangle</a>
</li>
<li>
<a href="https://msdn.microsoft.com/17808a6a-7bd0-4fd6-81ab-00d5db764b93">RoundRect</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/90f123e2-c3c7-4ba1-a42b-7d6bc0074d5b">Line and Curve Functions</a>



<a href="https://msdn.microsoft.com/8c65c185-8346-459e-bdf7-1cf3f7419736">Lines and Curves Overview</a>
 

 

