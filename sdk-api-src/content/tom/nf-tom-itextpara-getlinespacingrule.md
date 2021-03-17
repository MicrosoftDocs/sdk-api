---
UID: NF:tom.ITextPara.GetLineSpacingRule
title: ITextPara::GetLineSpacingRule (tom.h)
description: Retrieves the line-spacing rule for the text range.
helpviewer_keywords: ["GetLineSpacingRule","GetLineSpacingRule method [Windows Controls]","GetLineSpacingRule method [Windows Controls]","ITextPara interface","ITextPara interface [Windows Controls]","GetLineSpacingRule method","ITextPara.GetLineSpacingRule","ITextPara::GetLineSpacingRule","_win32_ITextPara_GetLineSpacingRule","_win32_ITextPara_GetLineSpacingRule_cpp","controls.ITextPara_GetLineSpacingRule","controls._win32_ITextPara_GetLineSpacingRule","tom/ITextPara::GetLineSpacingRule","tomLineSpace1pt5","tomLineSpaceAtLeast","tomLineSpaceDouble","tomLineSpaceExactly","tomLineSpaceMultiple","tomLineSpacePercent","tomLineSpaceSingle"]
old-location: controls\ITextPara_GetLineSpacingRule.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getlinespacingrule.htm
ms.date: 12/05/2018
ms.keywords: GetLineSpacingRule, GetLineSpacingRule method [Windows Controls], GetLineSpacingRule method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],GetLineSpacingRule method, ITextPara.GetLineSpacingRule, ITextPara::GetLineSpacingRule, _win32_ITextPara_GetLineSpacingRule, _win32_ITextPara_GetLineSpacingRule_cpp, controls.ITextPara_GetLineSpacingRule, controls._win32_ITextPara_GetLineSpacingRule, tom/ITextPara::GetLineSpacingRule, tomLineSpace1pt5, tomLineSpaceAtLeast, tomLineSpaceDouble, tomLineSpaceExactly, tomLineSpaceMultiple, tomLineSpacePercent, tomLineSpaceSingle
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
 - ITextPara::GetLineSpacingRule
 - tom/ITextPara::GetLineSpacingRule
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
 - ITextPara.GetLineSpacingRule
---

# ITextPara::GetLineSpacingRule


## -description

Retrieves the line-spacing rule for the text range.

## -parameters

### -param pValue

Type: <b>long*</b>

A variable that is one of the following values to indicate the line-spacing rule. 
					

<a id="tomLineSpaceSingle"></a>
<a id="tomlinespacesingle"></a>
<a id="TOMLINESPACESINGLE"></a>


#### tomLineSpaceSingle

<a id="tomLineSpace1pt5"></a>
<a id="tomlinespace1pt5"></a>
<a id="TOMLINESPACE1PT5"></a>


#### tomLineSpace1pt5

<a id="tomLineSpaceDouble"></a>
<a id="tomlinespacedouble"></a>
<a id="TOMLINESPACEDOUBLE"></a>


#### tomLineSpaceDouble

<a id="tomLineSpaceAtLeast"></a>
<a id="tomlinespaceatleast"></a>
<a id="TOMLINESPACEATLEAST"></a>


#### tomLineSpaceAtLeast

<a id="tomLineSpaceExactly"></a>
<a id="tomlinespaceexactly"></a>
<a id="TOMLINESPACEEXACTLY"></a>


#### tomLineSpaceExactly

<a id="tomLineSpaceMultiple"></a>
<a id="tomlinespacemultiple"></a>
<a id="TOMLINESPACEMULTIPLE"></a>


#### tomLineSpaceMultiple

<a id="tomLineSpacePercent"></a>
<a id="tomlinespacepercent"></a>
<a id="TOMLINESPACEPERCENT"></a>


#### tomLineSpacePercent

## -returns

Type: <b>HRESULT</b>

If <b>ITextPara::GetLineSpacingRule</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-getlinespacing">GetLineSpacing</a>



<a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-setlinespacing">SetLineSpacing</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>