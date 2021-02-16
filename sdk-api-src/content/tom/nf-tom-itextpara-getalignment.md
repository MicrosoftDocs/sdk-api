---
UID: NF:tom.ITextPara.GetAlignment
title: ITextPara::GetAlignment (tom.h)
description: Retrieves the current paragraph alignment value.
helpviewer_keywords: ["GetAlignment","GetAlignment method [Windows Controls]","GetAlignment method [Windows Controls]","ITextPara interface","ITextPara interface [Windows Controls]","GetAlignment method","ITextPara.GetAlignment","ITextPara::GetAlignment","_win32_ITextPara_GetAlignment","_win32_ITextPara_GetAlignment_cpp","controls.ITextPara_GetAlignment","controls._win32_ITextPara_GetAlignment","tom/ITextPara::GetAlignment","tomAlignCenter","tomAlignInterLetter","tomAlignInterWord","tomAlignJustify","tomAlignLeft","tomAlignNewspaper","tomAlignRight","tomAlignScaled"]
old-location: controls\ITextPara_GetAlignment.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getalignment.htm
ms.date: 12/05/2018
ms.keywords: GetAlignment, GetAlignment method [Windows Controls], GetAlignment method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],GetAlignment method, ITextPara.GetAlignment, ITextPara::GetAlignment, _win32_ITextPara_GetAlignment, _win32_ITextPara_GetAlignment_cpp, controls.ITextPara_GetAlignment, controls._win32_ITextPara_GetAlignment, tom/ITextPara::GetAlignment, tomAlignCenter, tomAlignInterLetter, tomAlignInterWord, tomAlignJustify, tomAlignLeft, tomAlignNewspaper, tomAlignRight, tomAlignScaled
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
 - ITextPara::GetAlignment
 - tom/ITextPara::GetAlignment
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
 - ITextPara.GetAlignment
---

# ITextPara::GetAlignment


## -description

Retrieves the current paragraph alignment value.

## -parameters

### -param pValue

Type: <b>long*</b>

The paragraph alignment, which can be one of the following values.

<a id="tomAlignLeft"></a>
<a id="tomalignleft"></a>
<a id="TOMALIGNLEFT"></a>


#### tomAlignLeft

<a id="tomAlignCenter"></a>
<a id="tomaligncenter"></a>
<a id="TOMALIGNCENTER"></a>


#### tomAlignCenter

<a id="tomAlignRight"></a>
<a id="tomalignright"></a>
<a id="TOMALIGNRIGHT"></a>


#### tomAlignRight

<a id="tomAlignJustify"></a>
<a id="tomalignjustify"></a>
<a id="TOMALIGNJUSTIFY"></a>


#### tomAlignJustify

<a id="tomAlignInterWord"></a>
<a id="tomaligninterword"></a>
<a id="TOMALIGNINTERWORD"></a>


#### tomAlignInterWord

<a id="tomAlignNewspaper"></a>
<a id="tomalignnewspaper"></a>
<a id="TOMALIGNNEWSPAPER"></a>


#### tomAlignNewspaper

<a id="tomAlignInterLetter"></a>
<a id="tomaligninterletter"></a>
<a id="TOMALIGNINTERLETTER"></a>


#### tomAlignInterLetter

<a id="tomAlignScaled"></a>
<a id="tomalignscaled"></a>
<a id="TOMALIGNSCALED"></a>


#### tomAlignScaled

## -returns

Type: <b>HRESULT</b>

If <b>ITextPara::GetAlignment</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes.  For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
The <i>pValue</i> parameter is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_RELEASED</b></dt>
</dl>
</td>
<td width="60%">
The paragraph format object is attached to a range that has been deleted.

</td>
</tr>
</table>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-setalignment">SetAlignment</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>