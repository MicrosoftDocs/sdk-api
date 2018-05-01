---
UID: NF:tom.ITextFont.SetBackColor
title: ITextFont::SetBackColor method
author: windows-driver-content
description: Sets the background color.
old-location: controls\ITextFont_SetBackColor.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setbackcolor.htm
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: ITextFont, ITextFont interface [Windows Controls], SetBackColor method, ITextFont::SetBackColor, SetBackColor method [Windows Controls], SetBackColor method [Windows Controls], ITextFont interface, SetBackColor,ITextFont.SetBackColor, _win32_ITextFont_SetBackColor, _win32_ITextFont_SetBackColor_cpp, controls.ITextFont_SetBackColor, controls._win32_ITextFont_SetBackColor, tom/ITextFont::SetBackColor
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MANCODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextFont.SetBackColor
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont::SetBackColor method


## -description


Sets the background color.


## -parameters




### -param Value [in]

Type: <b>long</b>

The new background color. It can be one of the following. 
					

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>A <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> value.</td>
<td>An RGB color.</td>
</tr>
<tr>
<td>A value returned by <a href="https://msdn.microsoft.com/76d859fa-11a5-451f-9d7a-9cf0740eca36">PALETTEINDEX</a>
</td>
<td>A palette index.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>No change.</td>
</tr>
<tr>
<td><b>tomAutoColor</b></td>
<td>Use the default background color.</td>
</tr>
</table>
 

If <i>Value</i> contains an RGB color, generate the <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> by using the <a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a> macro.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Write access is denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/b5925136-b883-4036-acee-29f640e8ee56">GetBackColor</a>



<a href="https://msdn.microsoft.com/e8e3ba98-808b-49c5-8764-96484fa33a6e">ITextFont</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/76d859fa-11a5-451f-9d7a-9cf0740eca36">PALETTEINDEX</a>



<a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

