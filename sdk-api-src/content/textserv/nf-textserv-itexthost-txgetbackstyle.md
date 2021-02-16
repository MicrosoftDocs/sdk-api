---
UID: NF:textserv.ITextHost.TxGetBackStyle
title: ITextHost::TxGetBackStyle (textserv.h)
description: Requests the background style of the text host.
helpviewer_keywords: ["ITextHost interface [Windows Controls]","TxGetBackStyle method","ITextHost.TxGetBackStyle","ITextHost::TxGetBackStyle","TXTBACK_OPAQUE","TXTBACK_TRANSPARENT","TxGetBackStyle","TxGetBackStyle method [Windows Controls]","TxGetBackStyle method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxGetBackStyle","_win32_ITextHost_TxGetBackStyle_cpp","controls.ITextHost_TxGetBackStyle","controls._win32_ITextHost_TxGetBackStyle","textserv/ITextHost::TxGetBackStyle"]
old-location: controls\ITextHost_TxGetBackStyle.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txgetbackstyle.htm
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxGetBackStyle method, ITextHost.TxGetBackStyle, ITextHost::TxGetBackStyle, TXTBACK_OPAQUE, TXTBACK_TRANSPARENT, TxGetBackStyle, TxGetBackStyle method [Windows Controls], TxGetBackStyle method [Windows Controls],ITextHost interface, _win32_ITextHost_TxGetBackStyle, _win32_ITextHost_TxGetBackStyle_cpp, controls.ITextHost_TxGetBackStyle, controls._win32_ITextHost_TxGetBackStyle, textserv/ITextHost::TxGetBackStyle
req.header: textserv.h
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
 - ITextHost::TxGetBackStyle
 - textserv/ITextHost::TxGetBackStyle
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
 - ITextHost.TxGetBackStyle
---

# ITextHost::TxGetBackStyle


## -description

Requests the background style of the text host.

## -parameters

### -param pstyle

Type: <b>TXTBACKSTYLE*</b>

A variable that the text host sets to indicate the background style. The style is one of the following values from the 
					<b>TXTBACKSTYLE</b> enumeration.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TXTBACK_TRANSPARENT"></a><a id="txtback_transparent"></a><dl>
<dt><b>TXTBACK_TRANSPARENT</b></dt>
</dl>
</td>
<td width="60%">
Background shows through. 

</td>
</tr>
<tr>
<td width="40%"><a id="TXTBACK_OPAQUE"></a><a id="txtback_opaque"></a><dl>
<dt><b>TXTBACK_OPAQUE</b></dt>
</dl>
</td>
<td width="60%">
Background does not show through. 

</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

The return value is <b>S_OK</b>.

## -see-also

<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls Overview</a>