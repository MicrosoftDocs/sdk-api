---
UID: NF:textserv.ITextHost.TxImmReleaseContext
title: ITextHost::TxImmReleaseContext (textserv.h)
description: Releases an input context returned by the ITextHost::TxImmGetContext method and unlocks the memory associated with the context. This method is used only in Asian-language versions of the operating system.
helpviewer_keywords: ["ITextHost interface [Windows Controls]","TxImmReleaseContext method","ITextHost.TxImmReleaseContext","ITextHost::TxImmReleaseContext","TxImmReleaseContext","TxImmReleaseContext method [Windows Controls]","TxImmReleaseContext method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxImmReleaseContext","_win32_ITextHost_TxImmReleaseContext_cpp","controls.ITextHost_TxImmReleaseContext","controls._win32_ITextHost_TxImmReleaseContext","textserv/ITextHost::TxImmReleaseContext"]
old-location: controls\ITextHost_TxImmReleaseContext.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost\itexthosttximmreleasecontext.htm
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxImmReleaseContext method, ITextHost.TxImmReleaseContext, ITextHost::TxImmReleaseContext, TxImmReleaseContext, TxImmReleaseContext method [Windows Controls], TxImmReleaseContext method [Windows Controls],ITextHost interface, _win32_ITextHost_TxImmReleaseContext, _win32_ITextHost_TxImmReleaseContext_cpp, controls.ITextHost_TxImmReleaseContext, controls._win32_ITextHost_TxImmReleaseContext, textserv/ITextHost::TxImmReleaseContext
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
 - ITextHost::TxImmReleaseContext
 - textserv/ITextHost::TxImmReleaseContext
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
 - ITextHost.TxImmReleaseContext
---

# ITextHost::TxImmReleaseContext


## -description

Releases an input context returned by the <a href="/windows/desktop/api/textserv/nf-textserv-itexthost-tximmgetcontext">ITextHost::TxImmGetContext</a> method and unlocks the memory associated with the context. 

This method is used only in Asian-language versions of the operating system.

## -parameters

### -param himc [in]

Type: <b>HIMC</b>

The input context.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<b>Reference</b>



<a href="/windows/desktop/api/textserv/nf-textserv-itexthost-tximmgetcontext">TxImmGetContext</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls</a>