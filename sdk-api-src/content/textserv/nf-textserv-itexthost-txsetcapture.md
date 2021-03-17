---
UID: NF:textserv.ITextHost.TxSetCapture
title: ITextHost::TxSetCapture (textserv.h)
description: Sets the mouse capture in the text host's window.
helpviewer_keywords: ["ITextHost interface [Windows Controls]","TxSetCapture method","ITextHost.TxSetCapture","ITextHost::TxSetCapture","TxSetCapture","TxSetCapture method [Windows Controls]","TxSetCapture method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxSetCapture","_win32_ITextHost_TxSetCapture_cpp","controls.ITextHost_TxSetCapture","controls._win32_ITextHost_TxSetCapture","textserv/ITextHost::TxSetCapture"]
old-location: controls\ITextHost_TxSetCapture.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost\itexthosttxsetcapture.htm
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxSetCapture method, ITextHost.TxSetCapture, ITextHost::TxSetCapture, TxSetCapture, TxSetCapture method [Windows Controls], TxSetCapture method [Windows Controls],ITextHost interface, _win32_ITextHost_TxSetCapture, _win32_ITextHost_TxSetCapture_cpp, controls.ITextHost_TxSetCapture, controls._win32_ITextHost_TxSetCapture, textserv/ITextHost::TxSetCapture
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
 - ITextHost::TxSetCapture
 - textserv/ITextHost::TxSetCapture
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
 - ITextHost.TxSetCapture
---

# ITextHost::TxSetCapture


## -description

Sets the mouse capture in the text host's window.

## -parameters

### -param fCapture [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Indicates whether to set or release the mouse capture. If <b>TRUE</b>, the mouse capture is set. If <b>FALSE</b>, the mouse capture is released.

## -remarks

This method is only valid when the control is in-place active; calls while the control is inactive may do nothing.

## -see-also

<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls Overview</a>