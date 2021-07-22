---
UID: NF:textserv.ITextHost2.TxGetEditStyle
title: ITextHost2::TxGetEditStyle (textserv.h)
description: Gets whether a rich edit control is in a dialog box.
helpviewer_keywords: ["ITextHost2 interface [Windows Controls]","TxGetEditStyle method","ITextHost2.TxGetEditStyle","ITextHost2::TxGetEditStyle","TXES_ISDIALOG","TxGetEditStyle","TxGetEditStyle method [Windows Controls]","TxGetEditStyle method [Windows Controls]","ITextHost2 interface","controls.itexthost2_txgeteditstyle","textserv/ITextHost2::TxGetEditStyle"]
old-location: controls\itexthost2_txgeteditstyle.htm
tech.root: Controls
ms.assetid: 8C5468C9-D152-4F57-9E8A-23B4852BFD69
ms.date: 12/05/2018
ms.keywords: ITextHost2 interface [Windows Controls],TxGetEditStyle method, ITextHost2.TxGetEditStyle, ITextHost2::TxGetEditStyle, TXES_ISDIALOG, TxGetEditStyle, TxGetEditStyle method [Windows Controls], TxGetEditStyle method [Windows Controls],ITextHost2 interface, controls.itexthost2_txgeteditstyle, textserv/ITextHost2::TxGetEditStyle
req.header: textserv.h
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
 - ITextHost2::TxGetEditStyle
 - textserv/ITextHost2::TxGetEditStyle
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
 - ITextHost2.TxGetEditStyle
---

# ITextHost2::TxGetEditStyle


## -description

Gets whether a rich edit control is in a dialog box.

## -parameters

### -param dwItem

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Mask that indicates the edit style flags to retrieve. It can be the following value.  

<a id="TXES_ISDIALOG"></a>
<a id="txes_isdialog"></a>


#### TXES_ISDIALOG

### -param pdwData

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a>*</b>

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TXES_ISDIALOG"></a><a id="txes_isdialog"></a><dl>
<dt><b>TXES_ISDIALOG</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the host of the rich edit control is a dialog box.

</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/textserv/nl-textserv-itexthost2">ITextHost2</a>