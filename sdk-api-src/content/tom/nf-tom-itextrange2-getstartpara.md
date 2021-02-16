---
UID: NF:tom.ITextRange2.GetStartPara
title: ITextRange2::GetStartPara (tom.h)
description: Gets the character position of the start of the paragraph that contains the range's start character position.
helpviewer_keywords: ["GetStartPara","GetStartPara method [Windows Controls]","GetStartPara method [Windows Controls]","ITextRange2 interface","ITextRange2 interface [Windows Controls]","GetStartPara method","ITextRange2.GetStartPara","ITextRange2::GetStartPara","controls.itextrange2_getstartpara","tom/ITextRange2::GetStartPara"]
old-location: controls\itextrange2_getstartpara.htm
tech.root: Controls
ms.assetid: c6a59ffd-0271-4c2a-9a9e-f31287b47ce9
ms.date: 12/05/2018
ms.keywords: GetStartPara, GetStartPara method [Windows Controls], GetStartPara method [Windows Controls],ITextRange2 interface, ITextRange2 interface [Windows Controls],GetStartPara method, ITextRange2.GetStartPara, ITextRange2::GetStartPara, controls.itextrange2_getstartpara, tom/ITextRange2::GetStartPara
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
 - ITextRange2::GetStartPara
 - tom/ITextRange2::GetStartPara
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
 - ITextRange2.GetStartPara
---

# ITextRange2::GetStartPara


## -description

Gets the character position of the start of the paragraph that contains the range's start character position.

## -parameters

### -param pValue [out, retval]

Type: <b>long*</b>

The start of the paragraph that contains the range's start character position.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>