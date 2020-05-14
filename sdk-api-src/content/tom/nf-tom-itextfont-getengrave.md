---
UID: NF:tom.ITextFont.GetEngrave
title: ITextFont::GetEngrave (tom.h)
description: Gets whether characters are displayed as imprinted characters.helpviewer_keywords: ["GetEngrave","GetEngrave method [Windows Controls]","GetEngrave method [Windows Controls]","ITextFont interface","ITextFont interface [Windows Controls]","GetEngrave method","ITextFont.GetEngrave","ITextFont::GetEngrave","_win32_ITextFont_GetEngrave","_win32_ITextFont_GetEngrave_cpp","controls.ITextFont_GetEngrave","controls._win32_ITextFont_GetEngrave","tom/ITextFont::GetEngrave"]
old-location: controls\ITextFont_GetEngrave.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getengrave.htm
ms.date: 12/05/2018
ms.keywords: GetEngrave, GetEngrave method [Windows Controls], GetEngrave method [Windows Controls],ITextFont interface, ITextFont interface [Windows Controls],GetEngrave method, ITextFont.GetEngrave, ITextFont::GetEngrave, _win32_ITextFont_GetEngrave, _win32_ITextFont_GetEngrave_cpp, controls.ITextFont_GetEngrave, controls._win32_ITextFont_GetEngrave, tom/ITextFont::GetEngrave
f1_keywords:
- tom/ITextFont.GetEngrave
dev_langs:
- c++
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
req.lib: 
req.dll: Msftedit.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Msftedit.dll
api_name:
- ITextFont.GetEngrave
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextFont::GetEngrave


## -description


Gets whether characters are displayed as imprinted characters.


## -parameters




### -param pValue

Type: <b>long*</b>

A <a href="https://docs.microsoft.com/windows/desktop/Controls/about-text-object-model">tomBool</a> value that can be one of the following.

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>tomTrue</b></td>
<td>Characters are displayed as imprinted characters.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Characters are not displayed as imprinted characters.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The Engrave property is undefined.</td>
</tr>
</table>
 


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://docs.microsoft.com/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
 




## -remarks



This property corresponds to the <b>CFE_IMPRINT</b> effect described in the <a href="https://docs.microsoft.com/windows/desktop/api/richedit/ns-richedit-charformat2a">CHARFORMAT2</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/richedit/ns-richedit-charformat2a">CHARFORMAT2</a>



<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-setengrave">SetEngrave</a>



<a href="https://docs.microsoft.com/windows/desktop/Controls/text-object-model">Text Object Model</a>
 

 

