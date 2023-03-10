---
UID: NF:tom.ITextDocument2.GetEastAsianFlags
title: ITextDocument2::GetEastAsianFlags (tom.h)
description: Gets the East Asian flags.
helpviewer_keywords: ["GetEastAsianFlags","GetEastAsianFlags method [Windows Controls]","GetEastAsianFlags method [Windows Controls]","ITextDocument2 interface","ITextDocument2 interface [Windows Controls]","GetEastAsianFlags method","ITextDocument2.GetEastAsianFlags","ITextDocument2::GetEastAsianFlags","controls.itextdocument2_geteastasianflags","tom/ITextDocument2::GetEastAsianFlags","tomNoIME","tomRE10Mode","tomSelfIME","tomTextFlowMask","tomUseAtFont","tomUsePassword"]
old-location: controls\itextdocument2_geteastasianflags.htm
tech.root: Controls
ms.assetid: 730c869d-cac0-40ce-b6c5-ca3be2c94419
ms.date: 12/05/2018
ms.keywords: GetEastAsianFlags, GetEastAsianFlags method [Windows Controls], GetEastAsianFlags method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetEastAsianFlags method, ITextDocument2.GetEastAsianFlags, ITextDocument2::GetEastAsianFlags, controls.itextdocument2_geteastasianflags, tom/ITextDocument2::GetEastAsianFlags, tomNoIME, tomRE10Mode, tomSelfIME, tomTextFlowMask, tomUseAtFont, tomUsePassword
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
 - ITextDocument2::GetEastAsianFlags
 - tom/ITextDocument2::GetEastAsianFlags
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
 - ITextDocument2.GetEastAsianFlags
---

# ITextDocument2::GetEastAsianFlags


## -description

Gets the East Asian flags.

## -parameters

### -param pFlags [out, retval]

Type: <b>long*</b>

The East Asian flags. This parameter can be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="tomRE10Mode"></a><a id="tomre10mode"></a><a id="TOMRE10MODE"></a><dl>
<dt><b>tomRE10Mode</b></dt>
</dl>
</td>
<td width="60%">
TOM version 1.0 emulation mode.

</td>
</tr>
<tr>
<td width="40%"><a id="tomUseAtFont"></a><a id="tomuseatfont"></a><a id="TOMUSEATFONT"></a><dl>
<dt><b>tomUseAtFont</b></dt>
</dl>
</td>
<td width="60%">
Use @ fonts for CJK vertical text.

</td>
</tr>
<tr>
<td width="40%"><a id="tomTextFlowMask"></a><a id="tomtextflowmask"></a><a id="TOMTEXTFLOWMASK"></a><dl>
<dt><b>tomTextFlowMask</b></dt>
</dl>
</td>
<td width="60%">
A mask for the following four text orientations:

<dl>
<dt><b>tomTextFlowES</b></dt>
<dd>
Ordinary left-to-right horizontal text.

</dd>
<dt><b>tomTextFlowSW</b></dt>
<dd>
Ordinary East Asian vertical text.

</dd>
<dt><b>tomTextFlowWN</b></dt>
<dd>
An alternative orientation.

</dd>
<dt><b>tomTextFlowNE</b></dt>
<dd>
An alternative orientation.

</dd>
</dl>
</td>
</tr>
<tr>
<td width="40%"><a id="tomUsePassword"></a><a id="tomusepassword"></a><a id="TOMUSEPASSWORD"></a><dl>
<dt><b>tomUsePassword</b></dt>
</dl>
</td>
<td width="60%">
Use password control.

</td>
</tr>
<tr>
<td width="40%"><a id="tomNoIME"></a><a id="tomnoime"></a><a id="TOMNOIME"></a><dl>
<dt><b>tomNoIME</b></dt>
</dl>
</td>
<td width="60%">
Turn off IME operation (see <a href="/windows/desktop/Controls/rich-edit-control-styles">ES_NOIME</a>).

</td>
</tr>
<tr>
<td width="40%"><a id="tomSelfIME"></a><a id="tomselfime"></a><a id="TOMSELFIME"></a><dl>
<dt><b>tomSelfIME</b></dt>
</dl>
</td>
<td width="60%">
The rich edit host handles IME operation (see <a href="/windows/desktop/Controls/rich-edit-control-styles">ES_SELFIME</a>) .

</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>