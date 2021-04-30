---
UID: NF:tom.ITextFont.GetName
title: ITextFont::GetName (tom.h)
description: Gets the font name.
helpviewer_keywords: ["GetName","GetName method [Windows Controls]","GetName method [Windows Controls]","ITextFont interface","ITextFont interface [Windows Controls]","GetName method","ITextFont.GetName","ITextFont::GetName","_win32_ITextFont_GetName","_win32_ITextFont_GetName_cpp","controls.ITextFont_GetName","controls._win32_ITextFont_GetName","tom/ITextFont::GetName"]
old-location: controls\ITextFont_GetName.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextfont\itextfontgetname.htm
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [Windows Controls], GetName method [Windows Controls],ITextFont interface, ITextFont interface [Windows Controls],GetName method, ITextFont.GetName, ITextFont::GetName, _win32_ITextFont_GetName, _win32_ITextFont_GetName_cpp, controls.ITextFont_GetName, controls._win32_ITextFont_GetName, tom/ITextFont::GetName
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextFont::GetName
 - tom/ITextFont::GetName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextFont.GetName
---

# ITextFont::GetName


## -description

Gets the font name.

## -parameters

### -param pbstr

Type: <b>BSTR*</b>

The font name.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Could not allocate memory for string.

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

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextfont-setname">SetName</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>