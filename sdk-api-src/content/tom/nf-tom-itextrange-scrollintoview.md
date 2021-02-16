---
UID: NF:tom.ITextRange.ScrollIntoView
title: ITextRange::ScrollIntoView (tom.h)
description: Scrolls the specified range into view.
helpviewer_keywords: ["ITextRange interface [Windows Controls]","ScrollIntoView method","ITextRange.ScrollIntoView","ITextRange::ScrollIntoView","ScrollIntoView","ScrollIntoView method [Windows Controls]","ScrollIntoView method [Windows Controls]","ITextRange interface","_win32_ITextRange_ScrollIntoView","_win32_ITextRange_ScrollIntoView_cpp","controls.ITextRange_ScrollIntoView","controls._win32_ITextRange_ScrollIntoView","tom/ITextRange::ScrollIntoView","tomEnd","tomNoUpScroll","tomNoVpScroll","tomStart"]
old-location: controls\ITextRange_ScrollIntoView.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\scrollintoview.htm
ms.date: 12/05/2018
ms.keywords: ITextRange interface [Windows Controls],ScrollIntoView method, ITextRange.ScrollIntoView, ITextRange::ScrollIntoView, ScrollIntoView, ScrollIntoView method [Windows Controls], ScrollIntoView method [Windows Controls],ITextRange interface, _win32_ITextRange_ScrollIntoView, _win32_ITextRange_ScrollIntoView_cpp, controls.ITextRange_ScrollIntoView, controls._win32_ITextRange_ScrollIntoView, tom/ITextRange::ScrollIntoView, tomEnd, tomNoUpScroll, tomNoVpScroll, tomStart
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
 - ITextRange::ScrollIntoView
 - tom/ITextRange::ScrollIntoView
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
 - ITextRange.ScrollIntoView
---

# ITextRange::ScrollIntoView


## -description

Scrolls the specified range into view.

## -parameters

### -param Value

Type: <b>long</b>

Flag specifying the end to scroll into view. It can be one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="tomEnd"></a><a id="tomend"></a><a id="TOMEND"></a><dl>
<dt><b><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomEnd</a></b></dt>
</dl>
</td>
<td width="60%">
Scrolls the end character position to appear on the bottom line.

</td>
</tr>
<tr>
<td width="40%"><a id="tomStart"></a><a id="tomstart"></a><a id="TOMSTART"></a><dl>
<dt><b><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomStart</a></b></dt>
</dl>
</td>
<td width="60%">
Scrolls the start character position to appear on the top line. (Default value).

</td>
</tr>
<tr>
<td width="40%"><a id="tomNoUpScroll"></a><a id="tomnoupscroll"></a><a id="TOMNOUPSCROLL"></a><dl>
<dt><b><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomNoUpScroll</a></b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="tomNoVpScroll"></a><a id="tomnovpscroll"></a><a id="TOMNOVPSCROLL"></a><dl>
<dt><b><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomNoVpScroll</a></b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns S_FALSE.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>