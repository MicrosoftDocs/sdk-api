---
UID: NF:tom.ITextRange.Collapse
title: ITextRange::Collapse (tom.h)
description: Collapses the specified text range into a degenerate point at either the beginning or end of the range.
helpviewer_keywords: ["Collapse","Collapse method [Windows Controls]","Collapse method [Windows Controls]","ITextRange interface","ITextRange interface [Windows Controls]","Collapse method","ITextRange.Collapse","ITextRange::Collapse","_win32_ITextRange_Collapse","_win32_ITextRange_Collapse_cpp","controls.ITextRange_Collapse","controls._win32_ITextRange_Collapse","tom/ITextRange::Collapse","tomEnd or tomFalse","tomStart or tomTrue"]
old-location: controls\ITextRange_Collapse.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\collapse.htm
ms.date: 12/05/2018
ms.keywords: Collapse, Collapse method [Windows Controls], Collapse method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],Collapse method, ITextRange.Collapse, ITextRange::Collapse, _win32_ITextRange_Collapse, _win32_ITextRange_Collapse_cpp, controls.ITextRange_Collapse, controls._win32_ITextRange_Collapse, tom/ITextRange::Collapse, tomEnd or tomFalse, tomStart or tomTrue
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
 - ITextRange::Collapse
 - tom/ITextRange::Collapse
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
 - ITextRange.Collapse
---

# ITextRange::Collapse


## -description

Collapses the specified text range into a degenerate point at either the beginning or end of the range.

## -parameters

### -param bStart [in]

Type: <b>long</b>

Flag specifying the end to collapse at. It can be one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="tomStart_or_tomTrue"></a><a id="tomstart_or_tomtrue"></a><a id="TOMSTART_OR_TOMTRUE"></a><dl>
<dt><b>tomStart or tomTrue</b></dt>
</dl>
</td>
<td width="60%">
Range is collapsed to the start of the range. This is the default.
					

</td>
</tr>
<tr>
<td width="40%"><a id="tomEnd_or_tomFalse"></a><a id="tomend_or_tomfalse"></a><a id="TOMEND_OR_TOMFALSE"></a><dl>
<dt><b>tomEnd or tomFalse</b></dt>
</dl>
</td>
<td width="60%">
Range is collapsed to the end of the range.
					

</td>
</tr>
</table>

## -returns

Type: <b>HRESULT</b>

This method returns an 
						<b>HRESULT</b> value. If successful, it returns <b>S_OK</b>. Otherwise, it returns S_FALSE.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>