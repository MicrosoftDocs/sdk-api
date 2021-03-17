---
UID: NF:tom.ITextDocument2.GetStrings
title: ITextDocument2::GetStrings (tom.h)
description: Gets a collection of rich-text strings.
helpviewer_keywords: ["GetStrings","GetStrings method [Windows Controls]","GetStrings method [Windows Controls]","ITextDocument2 interface","ITextDocument2 interface [Windows Controls]","GetStrings method","ITextDocument2.GetStrings","ITextDocument2::GetStrings","controls.itextdocument2_getstrings","tom/ITextDocument2::GetStrings"]
old-location: controls\itextdocument2_getstrings.htm
tech.root: Controls
ms.assetid: 54d8c682-4e30-4ce2-baa1-d89e28491015
ms.date: 12/05/2018
ms.keywords: GetStrings, GetStrings method [Windows Controls], GetStrings method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetStrings method, ITextDocument2.GetStrings, ITextDocument2::GetStrings, controls.itextdocument2_getstrings, tom/ITextDocument2::GetStrings
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
 - ITextDocument2::GetStrings
 - tom/ITextDocument2::GetStrings
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
 - ITextDocument2.GetStrings
---

# ITextDocument2::GetStrings


## -description

Gets a collection of rich-text strings.

## -parameters

### -param ppStrs [out]

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextstrings">ITextStrings</a>**</b>

The collection of rich-text strings.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The collection is useful for manipulating rich text, particularly for transforming mathematical text from linear to built-up form, or vice versa.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>