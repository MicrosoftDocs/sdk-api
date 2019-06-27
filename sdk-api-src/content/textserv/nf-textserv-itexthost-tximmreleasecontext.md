---
UID: NF:textserv.ITextHost.TxImmReleaseContext
title: ITextHost::TxImmReleaseContext (textserv.h)
author: windows-sdk-content
description: Releases an input context returned by the ITextHost::TxImmGetContext method and unlocks the memory associated with the context. This method is used only in Asian-language versions of the operating system.
old-location: controls\ITextHost_TxImmReleaseContext.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost\itexthosttximmreleasecontext.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxImmReleaseContext method, ITextHost.TxImmReleaseContext, ITextHost::TxImmReleaseContext, TxImmReleaseContext, TxImmReleaseContext method [Windows Controls], TxImmReleaseContext method [Windows Controls],ITextHost interface, _win32_ITextHost_TxImmReleaseContext, _win32_ITextHost_TxImmReleaseContext_cpp, controls.ITextHost_TxImmReleaseContext, controls._win32_ITextHost_TxImmReleaseContext, textserv/ITextHost::TxImmReleaseContext
ms.topic: method
f1_keywords: 
 - "textserv/ITextHost.TxImmReleaseContext"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextHost.TxImmReleaseContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextHost::TxImmReleaseContext


## -description


Releases an input context returned by the <a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-tximmgetcontext">ITextHost::TxImmGetContext</a> method and unlocks the memory associated with the context. 

This method is used only in Asian-language versions of the operating system.


## -parameters




### -param himc [in]

Type: <b>HIMC</b>

The input context. 


## -returns



This method has no return value.




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itexthost-tximmgetcontext">TxImmGetContext</a>



<a href="https://docs.microsoft.com/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls</a>
 

 

