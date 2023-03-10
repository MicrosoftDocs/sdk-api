---
UID: NN:tom.ITextDocument2
title: ITextDocument2 (tom.h)
description: Extends the ITextDocument interface, adding methods that enable the Input Method Editor (IME) to drive the rich edit control, and methods to retrieve other interfaces such as ITextDisplays, ITextRange2, ITextFont2, ITextPara2, and so on.
helpviewer_keywords: ["ITextDocument2","ITextDocument2 interface [Windows Controls]","ITextDocument2 interface [Windows Controls]","described","controls.itextdocument2","tom/ITextDocument2"]
old-location: controls\itextdocument2.htm
tech.root: Controls
ms.assetid: 0b0a54d7-7606-41f6-b8be-6367d9180ef4
ms.date: 12/05/2018
ms.keywords: ITextDocument2, ITextDocument2 interface [Windows Controls], ITextDocument2 interface [Windows Controls],described, controls.itextdocument2, tom/ITextDocument2
req.header: tom.h
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
 - ITextDocument2
 - tom/ITextDocument2
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
 - ITextDocument2
---

# ITextDocument2 interface


## -description

Extends the <a href="/windows/desktop/api/tom/nn-tom-itextdocument">ITextDocument</a> interface, adding methods that enable the Input Method Editor (IME) to drive the rich edit control, and methods to retrieve other interfaces such as  <a href="/windows/desktop/api/tom/nn-tom-itextdisplays">ITextDisplays</a>, <a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>, <a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>, <a href="/windows/desktop/api/tom/nn-tom-itextpara2">ITextPara2</a>, and so on. 

Some <b>ITextDocument2</b> methods used with the IME need access to the current window handle (<b>HWND</b>). Use the <a href="/windows/desktop/api/tom/nf-tom-itextdocument2-getwindow">ITextDocument2::GetWindow</a> method to retrieve the handle.

## -inheritance

The <b>ITextDocument2</b> interface inherits from <b>ITextDocument</b>. <b>ITextDocument2</b> also has these types of members:

