---
UID: NF:tom.ITextRange2.GetFont2
title: ITextRange2::GetFont2 (tom.h)
description: Gets an ITextFont2 object with the character attributes of the current range.
helpviewer_keywords: ["GetFont2","GetFont2 method [Windows Controls]","GetFont2 method [Windows Controls]","ITextRange2 interface","ITextRange2 interface [Windows Controls]","GetFont2 method","ITextRange2.GetFont2","ITextRange2::GetFont2","controls.itextrange2_getfont2","tom/ITextRange2::GetFont2"]
old-location: controls\itextrange2_getfont2.htm
tech.root: Controls
ms.assetid: 24ef7fb3-4cf4-46ed-9273-6f91c77f7641
ms.date: 12/05/2018
ms.keywords: GetFont2, GetFont2 method [Windows Controls], GetFont2 method [Windows Controls],ITextRange2 interface, ITextRange2 interface [Windows Controls],GetFont2 method, ITextRange2.GetFont2, ITextRange2::GetFont2, controls.itextrange2_getfont2, tom/ITextRange2::GetFont2
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
 - ITextRange2::GetFont2
 - tom/ITextRange2::GetFont2
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
 - ITextRange2.GetFont2
---

# ITextRange2::GetFont2


## -description

Gets an <a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a> object with the character attributes of the current range.

## -parameters

### -param ppFont [out, retval]

Type: <b>ITextFont2**</b>

The <a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a> object.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange2-setfont2">ITextRange2::SetFont2</a>