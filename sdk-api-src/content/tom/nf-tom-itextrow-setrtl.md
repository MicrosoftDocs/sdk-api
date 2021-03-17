---
UID: NF:tom.ITextRow.SetRTL
title: ITextRow::SetRTL (tom.h)
description: Sets whether this row has right-to-left orientation.
helpviewer_keywords: ["ITextRow interface [Windows Controls]","SetRTL method","ITextRow.SetRTL","ITextRow::SetRTL","SetRTL","SetRTL method [Windows Controls]","SetRTL method [Windows Controls]","ITextRow interface","controls.itextrow_setrtl","tom/ITextRow::SetRTL","tomFalse","tomToggle","tomTrue"]
old-location: controls\itextrow_setrtl.htm
tech.root: Controls
ms.assetid: e260f989-6028-4cd2-a1e0-0eca2a5bd553
ms.date: 12/05/2018
ms.keywords: ITextRow interface [Windows Controls],SetRTL method, ITextRow.SetRTL, ITextRow::SetRTL, SetRTL, SetRTL method [Windows Controls], SetRTL method [Windows Controls],ITextRow interface, controls.itextrow_setrtl, tom/ITextRow::SetRTL, tomFalse, tomToggle, tomTrue
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - ITextRow::SetRTL
 - tom/ITextRow::SetRTL
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
 - ITextRow.SetRTL
---

# ITextRow::SetRTL


## -description

Sets whether this row has right-to-left orientation.

## -parameters

### -param Value [in]

Type: <b>long</b>


A <a href="/windows/desktop/Controls/about-text-object-model">tomBool</a> value that can be one of the following.



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
Right-to-left orientation.

</td>
</tr>
<tr>
<td width="40%"><a id="tomFalse"></a><a id="tomfalse"></a><a id="TOMFALSE"></a><dl>
<dt><b>tomFalse</b></dt>
</dl>
</td>
<td width="60%">
Left-to-right orientation.

</td>
</tr>
<tr>
<td width="40%"><a id="tomToggle"></a><a id="tomtoggle"></a><a id="TOMTOGGLE"></a><dl>
<dt><b>tomToggle</b></dt>
</dl>
</td>
<td width="60%">
Toggles the orientation.

</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-getrtl">ITextRow::GetRTL</a>