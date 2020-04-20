---
UID: NF:tom.ITextPara.GetKeepWithNext
title: ITextPara::GetKeepWithNext (tom.h)
description: Determines whether page breaks are allowed between paragraphs in the range.helpviewer_keywords: ["GetKeepWithNext","GetKeepWithNext method [Windows Controls]","GetKeepWithNext method [Windows Controls]","ITextPara interface","ITextPara interface [Windows Controls]","GetKeepWithNext method","ITextPara.GetKeepWithNext","ITextPara::GetKeepWithNext","_win32_ITextPara_GetKeepWithNext","_win32_ITextPara_GetKeepWithNext_cpp","controls.ITextPara_GetKeepWithNext","controls._win32_ITextPara_GetKeepWithNext","tom/ITextPara::GetKeepWithNext","tomFalse","tomTrue","tomUndefined"]
old-location: controls\ITextPara_GetKeepWithNext.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getkeepwithnext.htm
ms.date: 12/05/2018
ms.keywords: GetKeepWithNext, GetKeepWithNext method [Windows Controls], GetKeepWithNext method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],GetKeepWithNext method, ITextPara.GetKeepWithNext, ITextPara::GetKeepWithNext, _win32_ITextPara_GetKeepWithNext, _win32_ITextPara_GetKeepWithNext_cpp, controls.ITextPara_GetKeepWithNext, controls._win32_ITextPara_GetKeepWithNext, tom/ITextPara::GetKeepWithNext, tomFalse, tomTrue, tomUndefined
f1_keywords:
- tom/ITextPara.GetKeepWithNext
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
- ITextPara.GetKeepWithNext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextPara::GetKeepWithNext


## -description


Determines whether page breaks are allowed between paragraphs in the range.


## -parameters




### -param pValue

Type: <b>long*</b>

A variable that is one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="tomTrue"></a><a id="tomtrue"></a><a id="TOMTRUE"></a><dl>
<dt><b>tomTrue</b></dt>
</dl>
</td>
<td width="60%">
Page breaks are not allowed between paragraphs.

</td>
</tr>
<tr>
<td width="40%"><a id="tomFalse"></a><a id="tomfalse"></a><a id="TOMFALSE"></a><dl>
<dt><b>tomFalse</b></dt>
</dl>
</td>
<td width="60%">
Page breaks are allowed between paragraphs.

</td>
</tr>
<tr>
<td width="40%"><a id="tomUndefined"></a><a id="tomundefined"></a><a id="TOMUNDEFINED"></a><dl>
<dt><b>tomUndefined</b></dt>
</dl>
</td>
<td width="60%">
The property is undefined.

</td>
</tr>
</table>
 


## -returns



Type: <b>HRESULT</b>

If <b>ITextPara::GetKeepWithNext</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes.  For more information about COM error codes, see <a href="https://docs.microsoft.com/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
<dt><b>CO_E_RELEASED</b></dt>
</dl>
</td>
<td width="60%">
The paragraph formatting object is attached to a range that has been deleted.

</td>
</tr>
</table>
 




## -remarks



This property corresponds to the PFE_KEEPNEXT effect described in the <a href="https://docs.microsoft.com/windows/desktop/api/richedit/ns-richedit-paraformat2">PARAFORMAT2</a> structure. 




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<a href="https://docs.microsoft.com/windows/desktop/api/richedit/ns-richedit-paraformat2">PARAFORMAT2</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-setkeepwithnext">SetKeepWithNext</a>



<a href="https://docs.microsoft.com/windows/desktop/Controls/text-object-model">Text Object Model</a>
 

 

