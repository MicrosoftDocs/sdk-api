---
UID: NF:tom.ITextDocument2.GetVersion
title: ITextDocument2::GetVersion (tom.h)
description: Gets the version number of the Text Object Model (TOM) engine.
helpviewer_keywords: ["GetVersion","GetVersion method [Windows Controls]","GetVersion method [Windows Controls]","ITextDocument2 interface","ITextDocument2 interface [Windows Controls]","GetVersion method","ITextDocument2.GetVersion","ITextDocument2::GetVersion","controls.itextdocument2_getversion","tom/ITextDocument2::GetVersion"]
old-location: controls\itextdocument2_getversion.htm
tech.root: Controls
ms.assetid: 4cc4502b-4e7c-4561-b7d4-a248bf248a8a
ms.date: 12/05/2018
ms.keywords: GetVersion, GetVersion method [Windows Controls], GetVersion method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetVersion method, ITextDocument2.GetVersion, ITextDocument2::GetVersion, controls.itextdocument2_getversion, tom/ITextDocument2::GetVersion
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
 - ITextDocument2::GetVersion
 - tom/ITextDocument2::GetVersion
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
 - ITextDocument2.GetVersion
---

# ITextDocument2::GetVersion


## -description

Gets the version number of the Text Object Model (TOM) engine.

## -parameters

### -param pValue [out, retval]

Type: <b>long*</b>

The version number. Byte 3 gives the major version number, byte 2 the minor version number, and the low-order 16 bits give the build number.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextdocument2-getgenerator">ITextDocument2::GetGenerator</a>