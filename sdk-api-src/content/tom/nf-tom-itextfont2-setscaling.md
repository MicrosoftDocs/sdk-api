---
UID: NF:tom.ITextFont2.SetScaling
title: ITextFont2::SetScaling (tom.h)
description: Sets the font horizontal scaling percentage.
helpviewer_keywords: ["ITextFont2 interface [Windows Controls]","SetScaling method","ITextFont2.SetScaling","ITextFont2::SetScaling","SetScaling","SetScaling method [Windows Controls]","SetScaling method [Windows Controls]","ITextFont2 interface","controls.itextfont2_setscaling","tom/ITextFont2::SetScaling"]
old-location: controls\itextfont2_setscaling.htm
tech.root: Controls
ms.assetid: b5f26c0a-a1bd-4be8-84b8-92a6d0cfafdb
ms.date: 12/05/2018
ms.keywords: ITextFont2 interface [Windows Controls],SetScaling method, ITextFont2.SetScaling, ITextFont2::SetScaling, SetScaling, SetScaling method [Windows Controls], SetScaling method [Windows Controls],ITextFont2 interface, controls.itextfont2_setscaling, tom/ITextFont2::SetScaling
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
 - ITextFont2::SetScaling
 - tom/ITextFont2::SetScaling
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
 - ITextFont2.SetScaling
---

# ITextFont2::SetScaling


## -description

Sets the font horizontal scaling percentage.

## -parameters

### -param Value [in]

Type: <b>long</b>

The scaling percentage. Values from 0 through 255 are valid. For example, a value of 200 doubles the widths of characters while retaining the same height. A value of 0 has the same effect as a value of 100; that is, it turns scaling off.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextfont2-getscaling">ITextFont2::GetScaling</a>