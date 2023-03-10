---
UID: NF:tom.ITextDocument2.GetCallManager
title: ITextDocument2::GetCallManager (tom.h)
description: Gets the call manager.
helpviewer_keywords: ["GetCallManager","GetCallManager method [Windows Controls]","GetCallManager method [Windows Controls]","ITextDocument2 interface","ITextDocument2 interface [Windows Controls]","GetCallManager method","ITextDocument2.GetCallManager","ITextDocument2::GetCallManager","controls.itextdocument2_getcallmanager","tom/ITextDocument2::GetCallManager"]
old-location: controls\itextdocument2_getcallmanager.htm
tech.root: Controls
ms.assetid: 0a90e6f5-1231-45fc-868f-4f24ed195638
ms.date: 12/05/2018
ms.keywords: GetCallManager, GetCallManager method [Windows Controls], GetCallManager method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetCallManager method, ITextDocument2.GetCallManager, ITextDocument2::GetCallManager, controls.itextdocument2_getcallmanager, tom/ITextDocument2::GetCallManager
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
 - ITextDocument2::GetCallManager
 - tom/ITextDocument2::GetCallManager
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
 - ITextDocument2.GetCallManager
---

# ITextDocument2::GetCallManager


## -description

Gets the call manager.

## -parameters

### -param ppVoid [out, retval]

Type: <b>IUnknown**</b>

The call manager object.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The call manager object is opaque to the caller. The Text Object Model (TOM) engine uses the object to handle internal notifications for particular scenarios.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextdocument2-releasecallmanager">ITextDocument2::ReleaseCallManager</a>