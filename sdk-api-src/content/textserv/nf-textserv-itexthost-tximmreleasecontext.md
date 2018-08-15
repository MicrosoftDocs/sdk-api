---
UID: NF:textserv.ITextHost.TxImmReleaseContext
title: ITextHost::TxImmReleaseContext
author: windows-sdk-content
description: Releases an input context returned by the ITextHost::TxImmGetContext method and unlocks the memory associated with the context. This method is used only in Asian-language versions of the operating system.
old-location: controls\ITextHost_TxImmReleaseContext.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost\itexthosttximmreleasecontext.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextHost interface [Windows Controls],TxImmReleaseContext method, ITextHost.TxImmReleaseContext, ITextHost::TxImmReleaseContext, TxImmReleaseContext, TxImmReleaseContext method [Windows Controls], TxImmReleaseContext method [Windows Controls],ITextHost interface, _win32_ITextHost_TxImmReleaseContext, _win32_ITextHost_TxImmReleaseContext_cpp, controls.ITextHost_TxImmReleaseContext, controls._win32_ITextHost_TxImmReleaseContext, textserv/ITextHost::TxImmReleaseContext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: textserv.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TMGR_DIRECTION
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
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextHost::TxImmReleaseContext


## -description


Releases an input context returned by the <a href="https://msdn.microsoft.com/1dcca568-e38c-42aa-a66f-0660bac6c0b6">ITextHost::TxImmGetContext</a> method and unlocks the memory associated with the context. 

This method is used only in Asian-language versions of the operating system.


## -parameters




### -param himc [in]

Type: <b>HIMC</b>

The input context. 


## -returns



This method has no return value.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/28d86b94-2d36-4749-8954-3857bf6dbdac">ITextHost</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/1dcca568-e38c-42aa-a66f-0660bac6c0b6">TxImmGetContext</a>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls</a>
 

 

