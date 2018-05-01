---
UID: NF:tom.ITextFont.SetKerning
title: ITextFont::SetKerning method
author: windows-driver-content
description: Sets the minimum font size at which kerning occurs.
old-location: controls\ITextFont_SetKerning.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setkerning.htm
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: ITextFont, ITextFont interface [Windows Controls], SetKerning method, ITextFont::SetKerning, SetKerning method [Windows Controls], SetKerning method [Windows Controls], ITextFont interface, SetKerning,ITextFont.SetKerning, _win32_ITextFont_SetKerning, _win32_ITextFont_SetKerning_cpp, controls.ITextFont_SetKerning, controls._win32_ITextFont_SetKerning, tom/ITextFont::SetKerning
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
-	ITextFont.SetKerning
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont::SetKerning method


## -description


Sets the minimum font size at which kerning occurs.


## -parameters




### -param Value [in]

Type: <b>float</b>

The new value of the minimum kerning size, in floating-point points. 


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
 




## -remarks



If this value is zero, kerning is turned off. Positive values turn on pair kerning for font sizes greater than this kerning value. For example, the value 1 turns on kerning for all legible sizes, whereas 16 turns on kerning only for font sizes of 16 points and larger.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/c7af7356-ada6-424c-bd8f-32c40a8c095c">GetKerning</a>



<a href="https://msdn.microsoft.com/e8e3ba98-808b-49c5-8764-96484fa33a6e">ITextFont</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

