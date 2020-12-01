---
UID: NF:tom.ITextDocument2.ReleaseCallManager
title: ITextDocument2::ReleaseCallManager (tom.h)
description: Releases the call manager.
helpviewer_keywords: ["ITextDocument2 interface [Windows Controls]","ReleaseCallManager method","ITextDocument2.ReleaseCallManager","ITextDocument2::ReleaseCallManager","ReleaseCallManager","ReleaseCallManager method [Windows Controls]","ReleaseCallManager method [Windows Controls]","ITextDocument2 interface","controls.itextdocument2_releasecallmanager","tom/ITextDocument2::ReleaseCallManager"]
old-location: controls\itextdocument2_releasecallmanager.htm
tech.root: Controls
ms.assetid: 4d17fdcb-502c-43ab-9f74-7247a1f14f45
ms.date: 12/05/2018
ms.keywords: ITextDocument2 interface [Windows Controls],ReleaseCallManager method, ITextDocument2.ReleaseCallManager, ITextDocument2::ReleaseCallManager, ReleaseCallManager, ReleaseCallManager method [Windows Controls], ReleaseCallManager method [Windows Controls],ITextDocument2 interface, controls.itextdocument2_releasecallmanager, tom/ITextDocument2::ReleaseCallManager
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
 - ITextDocument2::ReleaseCallManager
 - tom/ITextDocument2::ReleaseCallManager
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
 - ITextDocument2.ReleaseCallManager
---

# ITextDocument2::ReleaseCallManager


## -description

Releases the call manager.

## -parameters

### -param pVoid [in]

Type: <b>IUnknown*</b>

The call manager object to release.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextdocument2-getcallmanager">ITextDocument2::GetCallManager</a>