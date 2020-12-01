---
UID: NF:tom.ITextRange2.GetDropCap
title: ITextRange2::GetDropCap (tom.h)
description: Gets the drop-cap parameters of the paragraph that contains this range.
helpviewer_keywords: ["GetDropCap","GetDropCap method [Windows Controls]","GetDropCap method [Windows Controls]","ITextRange2 interface","ITextRange2 interface [Windows Controls]","GetDropCap method","ITextRange2.GetDropCap","ITextRange2::GetDropCap","controls.itextrange2_getdropcap","tom/ITextRange2::GetDropCap"]
old-location: controls\itextrange2_getdropcap.htm
tech.root: Controls
ms.assetid: c653c002-6708-4813-83ae-1ea578bdcee2
ms.date: 12/05/2018
ms.keywords: GetDropCap, GetDropCap method [Windows Controls], GetDropCap method [Windows Controls],ITextRange2 interface, ITextRange2 interface [Windows Controls],GetDropCap method, ITextRange2.GetDropCap, ITextRange2::GetDropCap, controls.itextrange2_getdropcap, tom/ITextRange2::GetDropCap
req.header: tom.h
req.include-header: Tom.h
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
 - ITextRange2::GetDropCap
 - tom/ITextRange2::GetDropCap
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
 - ITextRange2.GetDropCap
---

# ITextRange2::GetDropCap


## -description

Not implemented.

Gets the drop-cap parameters of the paragraph that contains this range.

## -parameters

### -param pcLine [out]

Type: <b>long*</b>

The count of lines for the drop cap.  A value of 0 means no drop cap.

### -param pPosition [out]

Type: <b>long*</b>

The position of the drop cap. The position can be one of the following: 

<ul>
<li>tomDropMargin</li>
<li>tomDropNone</li>
<li>tomDropNormal</li>
</ul>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange2-setdropcap">ITextRange2::SetDropCap</a>