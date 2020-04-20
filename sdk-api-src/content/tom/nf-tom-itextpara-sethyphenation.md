---
UID: NF:tom.ITextPara.SetHyphenation
title: ITextPara::SetHyphenation (tom.h)
description: Controls hyphenation for the paragraphs in the range.helpviewer_keywords: ["ITextPara interface [Windows Controls]","SetHyphenation method","ITextPara.SetHyphenation","ITextPara::SetHyphenation","SetHyphenation","SetHyphenation method [Windows Controls]","SetHyphenation method [Windows Controls]","ITextPara interface","_win32_ITextPara_SetHyphenation","_win32_ITextPara_SetHyphenation_cpp","controls.ITextPara_SetHyphenation","controls._win32_ITextPara_SetHyphenation","tom/ITextPara::SetHyphenation"]
old-location: controls\ITextPara_SetHyphenation.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\sethyphenation.htm
ms.date: 12/05/2018
ms.keywords: ITextPara interface [Windows Controls],SetHyphenation method, ITextPara.SetHyphenation, ITextPara::SetHyphenation, SetHyphenation, SetHyphenation method [Windows Controls], SetHyphenation method [Windows Controls],ITextPara interface, _win32_ITextPara_SetHyphenation, _win32_ITextPara_SetHyphenation_cpp, controls.ITextPara_SetHyphenation, controls._win32_ITextPara_SetHyphenation, tom/ITextPara::SetHyphenation
f1_keywords:
- tom/ITextPara.SetHyphenation
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
- ITextPara.SetHyphenation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextPara::SetHyphenation


## -description


Controls hyphenation for the paragraphs in the range.


## -parameters




### -param Value [in]

Type: <b>long</b>

Indicates how hyphenation is controlled. It can be one of the following possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>tomTrue</dt>
</dl>
</td>
<td width="60%">
Automatic hyphenation is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>tomFalse</dt>
</dl>
</td>
<td width="60%">
Automatic hyphenation is disabled.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>tomUndefined</dt>
</dl>
</td>
<td width="60%">
The hyphenation property is undefined.

</td>
</tr>
</table>
 


## -returns



Type: <b>HRESULT</b>

If <b>ITextPara::SetHyphenation</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://docs.microsoft.com/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Value</b></dt>
</dl>
</td>
<td width="60%">
Meaning

</td>
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
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_RELEASED</b></dt>
</dl>
</td>
<td width="60%">
The paragraph formatting object is attached to a range that has been deleted.

</td>
</tr>
</table>
 




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-gethyphenation">GetHyphenation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/Controls/text-object-model">Text Object Model</a>
 

 

