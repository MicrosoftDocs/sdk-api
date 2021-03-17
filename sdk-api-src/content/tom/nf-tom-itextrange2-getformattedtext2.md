---
UID: NF:tom.ITextRange2.GetFormattedText2
title: ITextRange2::GetFormattedText2 (tom.h)
description: Gets an ITextRange2 object with the current range's formatted text.
helpviewer_keywords: ["GetFormattedText2","GetFormattedText2 method [Windows Controls]","GetFormattedText2 method [Windows Controls]","ITextRange2 interface","ITextRange2 interface [Windows Controls]","GetFormattedText2 method","ITextRange2.GetFormattedText2","ITextRange2::GetFormattedText2","controls.itextrange2_getformattedtext2","tom/ITextRange2::GetFormattedText2"]
old-location: controls\itextrange2_getformattedtext2.htm
tech.root: Controls
ms.assetid: 9fe5d82d-b13e-4b94-beb6-15691d4c5176
ms.date: 12/05/2018
ms.keywords: GetFormattedText2, GetFormattedText2 method [Windows Controls], GetFormattedText2 method [Windows Controls],ITextRange2 interface, ITextRange2 interface [Windows Controls],GetFormattedText2 method, ITextRange2.GetFormattedText2, ITextRange2::GetFormattedText2, controls.itextrange2_getformattedtext2, tom/ITextRange2::GetFormattedText2
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
 - ITextRange2::GetFormattedText2
 - tom/ITextRange2::GetFormattedText2
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
 - ITextRange2.GetFormattedText2
---

# ITextRange2::GetFormattedText2


## -description

Gets an <a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a> object with the current range's formatted text.

## -parameters

### -param ppRange [out, retval]

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>**</b>

The formatted text.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange2-setformattedtext2">ITextRange2::SetFormattedText2</a>