---
UID: NF:wingdi.SetLayout
title: SetLayout function (wingdi.h)
author: windows-sdk-content
description: The SetLayout function changes the layout of a device context (DC).
old-location: gdi\setlayout.htm
tech.root: gdi
ms.assetid: 81c6dccd-cfb1-486f-8c25-f46ba7c3ff8d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: LAYOUT_BITMAPORIENTATIONPRESERVED, LAYOUT_RTL, SetLayout, SetLayout function [Windows GDI], _win32_SetLayout, gdi.setlayout, wingdi/SetLayout
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
 - Ext-MS-Win-GDI-Draw-l1-1-0.dll
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - SetLayout
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetLayout function


## -description


The <b>SetLayout</b> function changes the layout of a device context (DC).


## -parameters




### -param hdc [in]

A handle to the DC.


### -param l [in]

The DC layout. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LAYOUT_BITMAPORIENTATIONPRESERVED"></a><a id="layout_bitmaporientationpreserved"></a><dl>
<dt><b>LAYOUT_BITMAPORIENTATIONPRESERVED</b></dt>
</dl>
</td>
<td width="60%">
Disables any reflection during <a href="https://msdn.microsoft.com/d6a181e4-b6cf-44b7-bf47-4900272d6d72">BitBlt</a> and <a href="https://msdn.microsoft.com/5130c88e-08e8-4faa-a1cb-a8106c86cea0">StretchBlt</a> operations.

</td>
</tr>
<tr>
<td width="40%"><a id="LAYOUT_RTL"></a><a id="layout_rtl"></a><dl>
<dt><b>LAYOUT_RTL</b></dt>
</dl>
</td>
<td width="60%">
Sets the default horizontal layout to be right to left.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, it returns the previous layout of the DC.

If the function fails, it returns GDI_ERROR.




## -remarks



The layout specifies the order in which text and graphics are revealed in a window or a device context. The default is left to right. The <b>SetLayout</b> function changes this to be right to left, which is the standard in Arabic and Hebrew cultures.

Once the LAYOUT_RTL flag is selected, flags normally specifying right or left are reversed. To avoid confusion, consider defining alternate words for standard flags, such as those in the following table.

<table>
<tr>
<th>Standard flag</th>
<th>Suggested alternate name</th>
</tr>
<tr>
<td>WS_EX_RIGHT</td>
<td>WS_EX_TRAILING</td>
</tr>
<tr>
<td>WS_EX_RTLREADING</td>
<td>WS_EX_REVERSEREADING</td>
</tr>
<tr>
<td>WS_EX_LEFTSCROLLBAR</td>
<td>WS_EX_LEADSCROLLBAR</td>
</tr>
<tr>
<td>ES_LEFT</td>
<td>ES_LEAD</td>
</tr>
<tr>
<td>ES_RIGHT</td>
<td>ES_TRAIL</td>
</tr>
<tr>
<td>EC_LEFTMARGIN</td>
<td>EC_LEADMARGIN</td>
</tr>
<tr>
<td>EC_RIGHTMARGIN</td>
<td>EC_TRAILMARGIN</td>
</tr>
</table>
 

<b>SetLayout</b> cannot modify drawing directly into the bits of a DIB.

For more information, see "Window Layout and Mirroring" in <a href="https://msdn.microsoft.com/en-us/library/ms632599(v=VS.85).aspx">Window Features</a>.




## -see-also




<a href="https://msdn.microsoft.com/9ff68d16-0f27-4cc8-932a-b2063cfed135">Device Context Functions</a>



<a href="https://msdn.microsoft.com/1fa97368-8931-4687-b37f-ed4db949a150">Device Contexts Overview</a>



<a href="https://msdn.microsoft.com/2bbc0bef-55e5-4f11-a195-d379e95e44bf">GetLayout
      </a>
 

 

