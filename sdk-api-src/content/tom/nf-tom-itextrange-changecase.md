---
UID: NF:tom.ITextRange.ChangeCase
title: ITextRange::ChangeCase (tom.h)
description: Changes the case of letters in this range according to the Type parameter.
helpviewer_keywords: ["ChangeCase","ChangeCase method [Windows Controls]","ChangeCase method [Windows Controls]","ITextRange interface","ITextRange interface [Windows Controls]","ChangeCase method","ITextRange.ChangeCase","ITextRange::ChangeCase","_win32_ITextRange_ChangeCase","_win32_ITextRange_ChangeCase_cpp","controls.ITextRange_ChangeCase","controls._win32_ITextRange_ChangeCase","tom/ITextRange::ChangeCase","tomLowerCase","tomSentenceCase","tomTitleCase","tomToggleCase","tomUpperCase"]
old-location: controls\ITextRange_ChangeCase.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\changecase.htm
ms.date: 12/05/2018
ms.keywords: ChangeCase, ChangeCase method [Windows Controls], ChangeCase method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],ChangeCase method, ITextRange.ChangeCase, ITextRange::ChangeCase, _win32_ITextRange_ChangeCase, _win32_ITextRange_ChangeCase_cpp, controls.ITextRange_ChangeCase, controls._win32_ITextRange_ChangeCase, tom/ITextRange::ChangeCase, tomLowerCase, tomSentenceCase, tomTitleCase, tomToggleCase, tomUpperCase
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
 - ITextRange::ChangeCase
 - tom/ITextRange::ChangeCase
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
 - ITextRange.ChangeCase
---

# ITextRange::ChangeCase


## -description

Changes the case of letters in this range according to the 
			<i>Type</i> parameter.

## -parameters

### -param Type [in]

Type: <b>long</b>

Type of case change. The default value is <i>tomLower</i>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="tomLowerCase"></a><a id="tomlowercase"></a><a id="TOMLOWERCASE"></a><dl>
<dt><b>tomLowerCase</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Sets all text to lowercase.
						

</td>
</tr>
<tr>
<td width="40%"><a id="tomUpperCase"></a><a id="tomuppercase"></a><a id="TOMUPPERCASE"></a><dl>
<dt><b>tomUpperCase</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Sets all text to lowercase.
						

</td>
</tr>
<tr>
<td width="40%"><a id="tomTitleCase"></a><a id="tomtitlecase"></a><a id="TOMTITLECASE"></a><dl>
<dt><b>tomTitleCase</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Capitalizes the first letter of each word.
						

</td>
</tr>
<tr>
<td width="40%"><a id="tomSentenceCase"></a><a id="tomsentencecase"></a><a id="TOMSENTENCECASE"></a><dl>
<dt><b>tomSentenceCase</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Capitalizes the first letter of each sentence.
						

</td>
</tr>
<tr>
<td width="40%"><a id="tomToggleCase"></a><a id="tomtogglecase"></a><a id="TOMTOGGLECASE"></a><dl>
<dt><b>tomToggleCase</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Toggles the case of each letter.
						

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