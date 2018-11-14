---
UID: NF:textserv.ITextHost.TxImmReleaseContext
title: ITextHost::TxImmReleaseContext
author: windows-sdk-content
description: Releases an input context returned by the ITextHost::TxImmGetContext method and unlocks the memory associated with the context. This method is used only in Asian-language versions of the operating system.
old-location: controls\ITextHost_TxImmReleaseContext.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost\itexthosttximmreleasecontext.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ITextHost interface [Windows Controls],TxImmReleaseContext method, ITextHost.TxImmReleaseContext, ITextHost::TxImmReleaseContext, TxImmReleaseContext, TxImmReleaseContext method [Windows Controls], TxImmReleaseContext method [Windows Controls],ITextHost interface, _win32_ITextHost_TxImmReleaseContext, _win32_ITextHost_TxImmReleaseContext_cpp, controls.ITextHost_TxImmReleaseContext, controls._win32_ITextHost_TxImmReleaseContext, textserv/ITextHost::TxImmReleaseContext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
- apiref
: 
- COM
: 
- textserv.h
: 
- ITextHost.TxImmReleaseContext
: 
---

# ITextHost::TxImmReleaseContext


## -description


Releases an input context returned by the <a href="https://msdn.microsoft.com/en-us/library/Bb787702(v=VS.85).aspx">ITextHost::TxImmGetContext</a> method and unlocks the memory associated with the context. 

This method is used only in Asian-language versions of the operating system.


## -parameters




### -param himc [in]

Type: <b>HIMC</b>

The input context. 


## -returns



This method has no return value.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787615(v=VS.85).aspx">ITextHost</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787702(v=VS.85).aspx">TxImmGetContext</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787609(v=VS.85).aspx">Windowless Rich Edit Controls</a>
 

 

