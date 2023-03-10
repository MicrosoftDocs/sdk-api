---
UID: NF:tom.ITextStory.GetActive
title: ITextStory::GetActive (tom.h)
description: Sets the active state of a story. (ITextStory.GetActive)
helpviewer_keywords: ["GetActive","GetActive method [Windows Controls]","GetActive method [Windows Controls]","ITextStory interface","ITextStory interface [Windows Controls]","GetActive method","ITextStory.GetActive","ITextStory::GetActive","controls.itextstory_getactive","tom/ITextStory::GetActive","tomDisplayActive","tomDisplayUIActive","tomInactive","tomUIActive"]
old-location: controls\itextstory_getactive.htm
tech.root: Controls
ms.assetid: 7bae9458-ee68-486a-a37f-2cc899400882
ms.date: 12/05/2018
ms.keywords: GetActive, GetActive method [Windows Controls], GetActive method [Windows Controls],ITextStory interface, ITextStory interface [Windows Controls],GetActive method, ITextStory.GetActive, ITextStory::GetActive, controls.itextstory_getactive, tom/ITextStory::GetActive, tomDisplayActive, tomDisplayUIActive, tomInactive, tomUIActive
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tom.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextStory::GetActive
 - tom/ITextStory::GetActive
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tom.h
api_name:
 - ITextStory.GetActive
---

# ITextStory::GetActive


## -description

Sets the active state of a story.

## -parameters

### -param pValue [out, retval]

Type: <b>long*</b>

The active state. It can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="tomDisplayActive"></a><a id="tomdisplayactive"></a><a id="TOMDISPLAYACTIVE"></a><dl>
<dt><b>tomDisplayActive</b></dt>
</dl>
</td>
<td width="60%">
The story has no UI or display (fast and lightweight).

</td>
</tr>
<tr>
<td width="40%"><a id="tomDisplayUIActive"></a><a id="tomdisplayuiactive"></a><a id="TOMDISPLAYUIACTIVE"></a><dl>
<dt><b>tomDisplayUIActive</b></dt>
</dl>
</td>
<td width="60%">
The story is UI active; that is, gets keyboard and mouse interactions.

</td>
</tr>
<tr>
<td width="40%"><a id="tomInactive"></a><a id="tominactive"></a><a id="TOMINACTIVE"></a><dl>
<dt><b>tomInactive</b></dt>
</dl>
</td>
<td width="60%">
The story has display, but no UI.

</td>
</tr>
<tr>
<td width="40%"><a id="tomUIActive"></a><a id="tomuiactive"></a><a id="TOMUIACTIVE"></a><dl>
<dt><b>tomUIActive</b></dt>
</dl>
</td>
<td width="60%">
The story has display and UI activity.

</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextstory">ITextStory</a>



<a href="/windows/desktop/api/tom/nf-tom-itextstory-setactive">ITextStory::SetActive</a>
