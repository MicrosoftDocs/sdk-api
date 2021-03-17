---
UID: NF:textserv.ITextHost.TxGetMaxLength
title: ITextHost::TxGetMaxLength (textserv.h)
description: Gets the text host's maximum allowed length for the text.
helpviewer_keywords: ["ITextHost interface [Windows Controls]","TxGetMaxLength method","ITextHost.TxGetMaxLength","ITextHost::TxGetMaxLength","TxGetMaxLength","TxGetMaxLength method [Windows Controls]","TxGetMaxLength method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxGetMaxLength","_win32_ITextHost_TxGetMaxLength_cpp","controls.ITextHost_TxGetMaxLength","controls._win32_ITextHost_TxGetMaxLength","textserv/ITextHost::TxGetMaxLength"]
old-location: controls\ITextHost_TxGetMaxLength.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txgetmaxlength.htm
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxGetMaxLength method, ITextHost.TxGetMaxLength, ITextHost::TxGetMaxLength, TxGetMaxLength, TxGetMaxLength method [Windows Controls], TxGetMaxLength method [Windows Controls],ITextHost interface, _win32_ITextHost_TxGetMaxLength, _win32_ITextHost_TxGetMaxLength_cpp, controls.ITextHost_TxGetMaxLength, controls._win32_ITextHost_TxGetMaxLength, textserv/ITextHost::TxGetMaxLength
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
 - ITextHost::TxGetMaxLength
 - textserv/ITextHost::TxGetMaxLength
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
 - ITextHost.TxGetMaxLength
---

# ITextHost::TxGetMaxLength


## -description

Gets the text host's maximum allowed length for the text.

## -parameters

### -param plength

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a>*</b>

The maximum allowed text length, in number of characters. If INFINITE is returned, the text services object can use as much memory as needed to store any specified text.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

The return value is <b>S_OK</b>.

## -remarks

When this maximum is reached, the text services object should reject any further character insertion and pasted text. 
				<a href="/windows/desktop/api/textserv/nf-textserv-itextservices-txsettext">TxSetText</a> however should still accept (and set) text longer than the maximum length. This is because this method is used for binding and is critical to maintaining the integrity of the data to which the control is bound.

This method parallels the <a href="/windows/desktop/Controls/em-limittext">EM_LIMITTEXT</a> message. 

If the limit returned is less than the number of characters currently in the text services object, no data is lost. Instead, no edits are allowed to the text 
				<i>other</i> than deletion until the text is reduced to below the limit.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/Controls/em-limittext">EM_LIMITTEXT</a>



<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls</a>