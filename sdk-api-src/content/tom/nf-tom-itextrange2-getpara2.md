---
UID: NF:tom.ITextRange2.GetPara2
title: ITextRange2::GetPara2 (tom.h)
description: Gets an ITextPara2 object with the paragraph attributes of a range.
helpviewer_keywords: ["GetPara2","GetPara2 method [Windows Controls]","GetPara2 method [Windows Controls]","ITextRange2 interface","ITextRange2 interface [Windows Controls]","GetPara2 method","ITextRange2.GetPara2","ITextRange2::GetPara2","controls.itextrange2_getpara2","tom/ITextRange2::GetPara2"]
old-location: controls\itextrange2_getpara2.htm
tech.root: Controls
ms.assetid: b20ebe85-f2a6-4a19-8b25-f1f16ebf5627
ms.date: 12/05/2018
ms.keywords: GetPara2, GetPara2 method [Windows Controls], GetPara2 method [Windows Controls],ITextRange2 interface, ITextRange2 interface [Windows Controls],GetPara2 method, ITextRange2.GetPara2, ITextRange2::GetPara2, controls.itextrange2_getpara2, tom/ITextRange2::GetPara2
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
 - ITextRange2::GetPara2
 - tom/ITextRange2::GetPara2
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
 - ITextRange2.GetPara2
---

# ITextRange2::GetPara2


## -description

Gets an <a href="/windows/desktop/api/tom/nn-tom-itextpara2">ITextPara2</a> object with the paragraph attributes of a range.

## -parameters

### -param ppPara [out, retval]

Type: <b>ITextPara2**</b>

The <a href="/windows/desktop/api/tom/nn-tom-itextpara2">ITextPara2</a> object.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange2-setpara2">ITextRange2::SetPara2</a>