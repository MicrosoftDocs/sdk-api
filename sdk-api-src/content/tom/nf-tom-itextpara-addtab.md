---
UID: NF:tom.ITextPara.AddTab
title: ITextPara::AddTab (tom.h)
description: Adds a tab at the displacement tbPos, with type tbAlign, and leader style, tbLeader.
helpviewer_keywords: ["AddTab","AddTab method [Windows Controls]","AddTab method [Windows Controls]","ITextPara interface","ITextPara interface [Windows Controls]","AddTab method","ITextPara.AddTab","ITextPara::AddTab","_win32_ITextPara_AddTab","_win32_ITextPara_AddTab_cpp","controls.ITextPara_AddTab","controls._win32_ITextPara_AddTab","tom/ITextPara::AddTab","tomAlignBar","tomAlignCenter","tomAlignDecimal","tomAlignLeft","tomAlignRight","tomDashes","tomDots","tomLines","tomSpaces"]
old-location: controls\ITextPara_AddTab.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\addtab.htm
ms.date: 12/05/2018
ms.keywords: AddTab, AddTab method [Windows Controls], AddTab method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],AddTab method, ITextPara.AddTab, ITextPara::AddTab, _win32_ITextPara_AddTab, _win32_ITextPara_AddTab_cpp, controls.ITextPara_AddTab, controls._win32_ITextPara_AddTab, tom/ITextPara::AddTab, tomAlignBar, tomAlignCenter, tomAlignDecimal, tomAlignLeft, tomAlignRight, tomDashes, tomDots, tomLines, tomSpaces
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
 - ITextPara::AddTab
 - tom/ITextPara::AddTab
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
 - ITextPara.AddTab
---

# ITextPara::AddTab


## -description

Adds a tab at the displacement 
			<i>tbPos</i>, with type 
			<i>tbAlign</i>, and leader style, 
			<i>tbLeader</i>.

## -parameters

### -param tbPos [in]

Type: <b>float</b>

New tab displacement, in floating-point points.

### -param tbAlign [in]

Type: <b>long</b>

Alignment options for the tab position. It can be one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="tomAlignLeft"></a><a id="tomalignleft"></a><a id="TOMALIGNLEFT"></a><dl>
<dt><b>tomAlignLeft</b></dt>
</dl>
</td>
<td width="60%">
Text is left justified from the tab position. This is the default.

</td>
</tr>
<tr>
<td width="40%"><a id="tomAlignCenter"></a><a id="tomaligncenter"></a><a id="TOMALIGNCENTER"></a><dl>
<dt><b>tomAlignCenter</b></dt>
</dl>
</td>
<td width="60%">
Text is centered on the tab position.

</td>
</tr>
<tr>
<td width="40%"><a id="tomAlignRight"></a><a id="tomalignright"></a><a id="TOMALIGNRIGHT"></a><dl>
<dt><b>tomAlignRight</b></dt>
</dl>
</td>
<td width="60%">
Text is right justified from the tab position.

</td>
</tr>
<tr>
<td width="40%"><a id="tomAlignDecimal"></a><a id="tomaligndecimal"></a><a id="TOMALIGNDECIMAL"></a><dl>
<dt><b>tomAlignDecimal</b></dt>
</dl>
</td>
<td width="60%">
The decimal point is set at the tab position. This is useful for aligning a column of decimal numbers.

</td>
</tr>
<tr>
<td width="40%"><a id="tomAlignBar"></a><a id="tomalignbar"></a><a id="TOMALIGNBAR"></a><dl>
<dt><b>tomAlignBar</b></dt>
</dl>
</td>
<td width="60%">
A vertical bar is positioned at the tab position. Text is not affected. Alignment bars on nearby lines at the same position form a continuous vertical line.

</td>
</tr>
</table>

### -param tbLeader [in]

Type: <b>long</b>

Leader character style. A leader character is the character that is used to fill the space taken by a tab character. It can be one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="tomSpaces"></a><a id="tomspaces"></a><a id="TOMSPACES"></a><dl>
<dt><b>tomSpaces</b></dt>
</dl>
</td>
<td width="60%">
Spaces are used. This is the default.

</td>
</tr>
<tr>
<td width="40%"><a id="tomDots"></a><a id="tomdots"></a><a id="TOMDOTS"></a><dl>
<dt><b>tomDots</b></dt>
</dl>
</td>
<td width="60%">
Dots are used.

</td>
</tr>
<tr>
<td width="40%"><a id="tomDashes"></a><a id="tomdashes"></a><a id="TOMDASHES"></a><dl>
<dt><b>tomDashes</b></dt>
</dl>
</td>
<td width="60%">
A dashed line is used.

</td>
</tr>
<tr>
<td width="40%"><a id="tomLines"></a><a id="tomlines"></a><a id="TOMLINES"></a><dl>
<dt><b>tomLines</b></dt>
</dl>
</td>
<td width="60%">
A solid line is used.

</td>
</tr>
</table>

## -returns

Type: <b>HRESULT</b>

If <b>ITextPara::AddTab</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes.  For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
The paragraph format object is attached to a range that has been deleted.

</td>
</tr>
</table>

## -remarks

It is assumed that there is never a tab at position zero. If multiple paragraphs are described, the common subset of tabs will be returned with 0x8000 in the upper word of the tab type.

## -see-also

<a href="/windows/desktop/api/tom/nf-tom-itextpara-clearalltabs">ClearAllTabs</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-deletetab">DeleteTab</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-getlisttab">GetListTab</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-gettab">GetTab</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-gettabcount">GetTabCount</a>



<a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-setlisttab">SetListTab</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>