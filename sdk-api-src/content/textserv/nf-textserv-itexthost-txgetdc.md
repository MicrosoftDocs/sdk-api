---
UID: NF:textserv.ITextHost.TxGetDC
title: ITextHost::TxGetDC (textserv.h)
description: Requests the device context for the text host window.
helpviewer_keywords: ["ITextHost interface [Windows Controls]","TxGetDC method","ITextHost.TxGetDC","ITextHost::TxGetDC","TxGetDC","TxGetDC method [Windows Controls]","TxGetDC method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxGetDC","_win32_ITextHost_TxGetDC_cpp","controls.ITextHost_TxGetDC","controls._win32_ITextHost_TxGetDC","textserv/ITextHost::TxGetDC"]
old-location: controls\ITextHost_TxGetDC.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txgetdc.htm
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxGetDC method, ITextHost.TxGetDC, ITextHost::TxGetDC, TxGetDC, TxGetDC method [Windows Controls], TxGetDC method [Windows Controls],ITextHost interface, _win32_ITextHost_TxGetDC, _win32_ITextHost_TxGetDC_cpp, controls.ITextHost_TxGetDC, controls._win32_ITextHost_TxGetDC, textserv/ITextHost::TxGetDC
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
 - ITextHost::TxGetDC
 - textserv/ITextHost::TxGetDC
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
 - ITextHost.TxGetDC
---

# ITextHost::TxGetDC


## -description

Requests the device context for the text host window.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a></b>

If the method succeeds, return the handle of the device context for the client area of the text host window. 

If the method fails, return <b>NULL</b>. For more information on COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

## -remarks

This method is only valid when the control is in-place active; calls while the control is inactive may fail.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getdc">GetDC</a>



<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<b>Other Resources</b>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls</a>
