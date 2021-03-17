---
UID: NF:tom.ITextRange.SetPara
title: ITextRange::SetPara (tom.h)
description: Sets the paragraph attributes of this range to those of the specified ITextPara object.
helpviewer_keywords: ["ITextRange interface [Windows Controls]","SetPara method","ITextRange.SetPara","ITextRange::SetPara","SetPara","SetPara method [Windows Controls]","SetPara method [Windows Controls]","ITextRange interface","_win32_ITextRange_SetPara","_win32_ITextRange_SetPara_cpp","controls.ITextRange_SetPara","controls._win32_ITextRange_SetPara","tom/ITextRange::SetPara"]
old-location: controls\ITextRange_SetPara.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setpara.htm
ms.date: 12/05/2018
ms.keywords: ITextRange interface [Windows Controls],SetPara method, ITextRange.SetPara, ITextRange::SetPara, SetPara, SetPara method [Windows Controls], SetPara method [Windows Controls],ITextRange interface, _win32_ITextRange_SetPara, _win32_ITextRange_SetPara_cpp, controls.ITextRange_SetPara, controls._win32_ITextRange_SetPara, tom/ITextRange::SetPara
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
 - ITextRange::SetPara
 - tom/ITextRange::SetPara
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
 - ITextRange.SetPara
---

# ITextRange::SetPara


## -description

Sets the paragraph attributes of this range to those of the specified <a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a> object.

## -parameters

### -param pPara [in]

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>*</b>

The paragraph object with the desired paragraph format.

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Text is write-protected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pPara</i> is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-getpara">GetPara</a>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>