---
UID: NF:tom.ITextDocument2.GetGenerator
title: ITextDocument2::GetGenerator (tom.h)
description: Gets the name of the Text Object Model (TOM) engine.
helpviewer_keywords: ["GetGenerator","GetGenerator method [Windows Controls]","GetGenerator method [Windows Controls]","ITextDocument2 interface","ITextDocument2 interface [Windows Controls]","GetGenerator method","ITextDocument2.GetGenerator","ITextDocument2::GetGenerator","controls.itextdocument2_getgenerator","tom/ITextDocument2::GetGenerator"]
old-location: controls\itextdocument2_getgenerator.htm
tech.root: Controls
ms.assetid: 22cfa44e-3603-458b-991e-6e536df63803
ms.date: 12/05/2018
ms.keywords: GetGenerator, GetGenerator method [Windows Controls], GetGenerator method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetGenerator method, ITextDocument2.GetGenerator, ITextDocument2::GetGenerator, controls.itextdocument2_getgenerator, tom/ITextDocument2::GetGenerator
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
 - ITextDocument2::GetGenerator
 - tom/ITextDocument2::GetGenerator
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
 - ITextDocument2.GetGenerator
---

# ITextDocument2::GetGenerator


## -description

Gets the name of the Text Object Model (TOM) engine.

## -parameters

### -param pbstr [out, retval]

Type: <b>BSTR*</b>

The name of the TOM engine.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>