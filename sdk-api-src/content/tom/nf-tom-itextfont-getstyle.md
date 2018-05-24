---
UID: NF:tom.ITextFont.GetStyle
title: ITextFont::GetStyle
author: windows-driver-content
description: Gets the character style handle of the characters in a range.
old-location: controls\ITextFont_GetStyle.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextfont\itextfontgetstyle.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetStyle, GetStyle method [Windows Controls], GetStyle method [Windows Controls],ITextFont interface, ITextFont interface [Windows Controls],GetStyle method, ITextFont.GetStyle, ITextFont::GetStyle, _win32_ITextFont_GetStyle, _win32_ITextFont_GetStyle_cpp, controls.ITextFont_GetStyle, controls._win32_ITextFont_GetStyle, tom/ITextFont::GetStyle
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
-	ITextFont.GetStyle
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont::GetStyle


## -description


Gets the character style handle of the characters in a range.


## -parameters




### -param pValue

Type: <b>long*</b>

The character style handle. 


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes.

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
The font object is attached to a range that was deleted.

</td>
</tr>
</table>
 

For more information on COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.




## -remarks



The Text Object Model (TOM) version 1.0 does not specify the meanings of the style handles. The meanings depend on other facilities of the text system that implements TOM. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e8e3ba98-808b-49c5-8764-96484fa33a6e">ITextFont</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/b2b39405-dd54-4873-a516-e4b7a865b465">SetStyle</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

