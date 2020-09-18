---
UID: NF:tom.ITextFont2.GetCookie
title: ITextFont2::GetCookie (tom.h)
description: Gets the client cookie.
helpviewer_keywords: ["GetCookie","GetCookie method [Windows Controls]","GetCookie method [Windows Controls]","ITextFont2 interface","ITextFont2 interface [Windows Controls]","GetCookie method","ITextFont2.GetCookie","ITextFont2::GetCookie","controls.itextfont2_getcookie","tom/ITextFont2::GetCookie"]
old-location: controls\itextfont2_getcookie.htm
tech.root: Controls
ms.assetid: f3e36338-8c88-4aaf-bbd0-c07a2228cb23
ms.date: 12/05/2018
ms.keywords: GetCookie, GetCookie method [Windows Controls], GetCookie method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetCookie method, ITextFont2.GetCookie, ITextFont2::GetCookie, controls.itextfont2_getcookie, tom/ITextFont2::GetCookie
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
 - ITextFont2::GetCookie
 - tom/ITextFont2::GetCookie
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
 - ITextFont2.GetCookie
---

# ITextFont2::GetCookie


## -description

Gets the client cookie.

## -parameters

### -param pValue [out, retval]

Type: <b>long*</b>

The client cookie.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This value is purely for the use of the client and has no meaning to the Text Object Model (TOM) engine. There are exceptions where different values correspond to different character format runs.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextfont2-setcookie">ITextFont2::SetCookie</a>