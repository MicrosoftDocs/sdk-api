---
UID: NF:textserv.ITextHost.TxClientToScreen
title: ITextHost::TxClientToScreen (textserv.h)
description: Converts text host coordinates to screen coordinates.
helpviewer_keywords: ["ITextHost interface [Windows Controls]","TxClientToScreen method","ITextHost.TxClientToScreen","ITextHost::TxClientToScreen","TxClientToScreen","TxClientToScreen method [Windows Controls]","TxClientToScreen method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxClientToScreen","_win32_ITextHost_TxClientToScreen_cpp","controls.ITextHost_TxClientToScreen","controls._win32_ITextHost_TxClientToScreen","textserv/ITextHost::TxClientToScreen"]
old-location: controls\ITextHost_TxClientToScreen.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txclienttoscreen.htm
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxClientToScreen method, ITextHost.TxClientToScreen, ITextHost::TxClientToScreen, TxClientToScreen, TxClientToScreen method [Windows Controls], TxClientToScreen method [Windows Controls],ITextHost interface, _win32_ITextHost_TxClientToScreen, _win32_ITextHost_TxClientToScreen_cpp, controls.ITextHost_TxClientToScreen, controls._win32_ITextHost_TxClientToScreen, textserv/ITextHost::TxClientToScreen
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
 - ITextHost::TxClientToScreen
 - textserv/ITextHost::TxClientToScreen
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
 - ITextHost.TxClientToScreen
---

# ITextHost::TxClientToScreen


## -description

Converts text host coordinates to screen coordinates.

## -parameters

### -param lppt [in]

Type: <b>LPPOINT</b>

The client coordinates to convert.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Return <b>TRUE</b> if the method succeeds. 

Return <b>FALSE</b> if the method fails.

## -remarks

This call is valid at any time, although it is allowed to fail. In general, if the text services object needs to translate from client coordinates (for example, for the TOM <a href="/windows/desktop/api/tom/nf-tom-itextrange-getpoint">GetPoint</a> method) the text services object is visible.

However, if no conversion is possible, then the method fails.

## -see-also

<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls Overview</a>