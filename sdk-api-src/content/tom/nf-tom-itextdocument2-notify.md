---
UID: NF:tom.ITextDocument2.Notify
title: ITextDocument2::Notify (tom.h)
description: Notifies the Text Object Model (TOM) engine client of particular Input Method Editor (IME) events.
helpviewer_keywords: ["ITextDocument2 interface [Windows Controls]","Notify method","ITextDocument2.Notify","ITextDocument2::Notify","Notify","Notify method [Windows Controls]","Notify method [Windows Controls]","ITextDocument2 interface","controls.itextdocument2_notify","tom/ITextDocument2::Notify"]
old-location: controls\itextdocument2_notify.htm
tech.root: Controls
ms.assetid: 5c7962a5-5f8d-4db1-bb94-a77738cf75bb
ms.date: 12/05/2018
ms.keywords: ITextDocument2 interface [Windows Controls],Notify method, ITextDocument2.Notify, ITextDocument2::Notify, Notify, Notify method [Windows Controls], Notify method [Windows Controls],ITextDocument2 interface, controls.itextdocument2_notify, tom/ITextDocument2::Notify
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
 - ITextDocument2::Notify
 - tom/ITextDocument2::Notify
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
 - ITextDocument2.Notify
---

# ITextDocument2::Notify


## -description

Notifies the Text Object Model (TOM) engine client of particular Input Method Editor (IME) events.

## -parameters

### -param Notify [in]

Type: <b>long</b>

An IME notification code.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>