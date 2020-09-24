---
UID: NF:tom.ITextFont2.GetAutospaceAlpha
title: ITextFont2::GetAutospaceAlpha (tom.h)
description: Gets the East Asian &quot;autospace alphabetics&quot; state.
helpviewer_keywords: ["GetAutospaceAlpha","GetAutospaceAlpha method [Windows Controls]","GetAutospaceAlpha method [Windows Controls]","ITextFont2 interface","ITextFont2 interface [Windows Controls]","GetAutospaceAlpha method","ITextFont2.GetAutospaceAlpha","ITextFont2::GetAutospaceAlpha","controls.itextfont2_getautospacealpha","tom/ITextFont2::GetAutospaceAlpha"]
old-location: controls\itextfont2_getautospacealpha.htm
tech.root: Controls
ms.assetid: 3f2070e9-2909-4642-ade2-54ef9af9cfc8
ms.date: 12/05/2018
ms.keywords: GetAutospaceAlpha, GetAutospaceAlpha method [Windows Controls], GetAutospaceAlpha method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetAutospaceAlpha method, ITextFont2.GetAutospaceAlpha, ITextFont2::GetAutospaceAlpha, controls.itextfont2_getautospacealpha, tom/ITextFont2::GetAutospaceAlpha
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
 - ITextFont2::GetAutospaceAlpha
 - tom/ITextFont2::GetAutospaceAlpha
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
 - ITextFont2.GetAutospaceAlpha
---

# ITextFont2::GetAutospaceAlpha


## -description

Gets the East Asian "autospace alphabetics" state.

## -parameters

### -param pValue [out, retval]

Type: <b>long*</b>

A <a href="/windows/desktop/Controls/about-text-object-model">tomBool</a> value that can be one of the following.

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>tomTrue</b></td>
<td>Use East Asian autospace alphabetics.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Do not use East Asian autospace alphabetics.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The AutospaceAlpha property is undefined.</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextfont2-setautospacealpha">ITextFont2::SetAutospaceAlpha</a>