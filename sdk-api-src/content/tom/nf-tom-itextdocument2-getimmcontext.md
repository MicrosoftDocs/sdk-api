---
UID: NF:tom.ITextDocument2.GetImmContext
title: ITextDocument2::GetImmContext (tom.h)
description: Gets the Input Method Manager (IMM) input context from the Text Object Model (TOM) host.
helpviewer_keywords: ["GetImmContext","GetImmContext method [Windows Controls]","GetImmContext method [Windows Controls]","ITextDocument2 interface","ITextDocument2 interface [Windows Controls]","GetImmContext method","ITextDocument2.GetImmContext","ITextDocument2::GetImmContext","controls.itextdocument2_getimmcontext","tom/ITextDocument2::GetImmContext"]
old-location: controls\itextdocument2_getimmcontext.htm
tech.root: Controls
ms.assetid: 42ee6d71-b51d-459a-b1af-638a19d8be2c
ms.date: 12/05/2018
ms.keywords: GetImmContext, GetImmContext method [Windows Controls], GetImmContext method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetImmContext method, ITextDocument2.GetImmContext, ITextDocument2::GetImmContext, controls.itextdocument2_getimmcontext, tom/ITextDocument2::GetImmContext
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
 - ITextDocument2::GetImmContext
 - tom/ITextDocument2::GetImmContext
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
 - ITextDocument2.GetImmContext
---

# ITextDocument2::GetImmContext


## -description

Gets the Input Method Manager (IMM) input context from the Text Object Model (TOM) host.

## -parameters

### -param pContext [out, retval]

Type: <b>__int64*</b>

The IMM input context.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextdocument2-releaseimmcontext">ITextDocument2::ReleaseIMMContext</a>