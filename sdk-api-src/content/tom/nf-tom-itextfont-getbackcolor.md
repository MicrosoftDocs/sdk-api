---
UID: NF:tom.ITextFont.GetBackColor
title: ITextFont::GetBackColor
author: windows-sdk-content
description: Gets the text background (highlight) color.
old-location: controls\ITextFont_GetBackColor.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getbackcolor.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetBackColor, GetBackColor method [Windows Controls], GetBackColor method [Windows Controls],ITextFont interface, ITextFont interface [Windows Controls],GetBackColor method, ITextFont.GetBackColor, ITextFont::GetBackColor, _win32_ITextFont_GetBackColor, _win32_ITextFont_GetBackColor_cpp, controls.ITextFont_GetBackColor, controls._win32_ITextFont_GetBackColor, tom/ITextFont::GetBackColor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: MANCODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextFont.GetBackColor
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont::GetBackColor


## -description


Gets the text background (highlight) color.


## -parameters




### -param pValue

Type: <b>long*</b>

The text background color. It can be one of the following values. 
					

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>A <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> value</td>
<td>The high-order byte is zero, and the three low-order bytes specify an RGB color. </td>
</tr>
<tr>
<td>A value returned by <a href="https://msdn.microsoft.com/76d859fa-11a5-451f-9d7a-9cf0740eca36">PALETTEINDEX</a>
</td>
<td>The high-order byte is 1, and the <a href="https://msdn.microsoft.com/library/ms632659(v=VS.85).aspx">LOWORD</a> specifies the index of a logical-color palette entry.</td>
</tr>
<tr>
<td><b>tomAutocolor</b> (-9999997)</td>
<td>Indicates the range uses the default system background color.</td>
</tr>
</table>
 


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_RELEASED</b></dt>
</dl>
</td>
<td width="60%">
The font object is attached to a range that has been deleted.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/Bb774054(v=VS.85).aspx">ITextFont</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/76d859fa-11a5-451f-9d7a-9cf0740eca36">PALETTEINDEX</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/Bb774129(v=VS.85).aspx">SetBackColor</a>



<a href="https://msdn.microsoft.com/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

