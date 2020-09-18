---
UID: NF:tom.ITextFont2.GetScaling
title: ITextFont2::GetScaling (tom.h)
description: Gets the font horizontal scaling percentage.
helpviewer_keywords: ["GetScaling","GetScaling method [Windows Controls]","GetScaling method [Windows Controls]","ITextFont2 interface","ITextFont2 interface [Windows Controls]","GetScaling method","ITextFont2.GetScaling","ITextFont2::GetScaling","controls.itextfont2_getscaling","tom/ITextFont2::GetScaling"]
old-location: controls\itextfont2_getscaling.htm
tech.root: Controls
ms.assetid: 4508d079-6f75-4842-a7e6-c2b9a99c826c
ms.date: 12/05/2018
ms.keywords: GetScaling, GetScaling method [Windows Controls], GetScaling method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetScaling method, ITextFont2.GetScaling, ITextFont2::GetScaling, controls.itextfont2_getscaling, tom/ITextFont2::GetScaling
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
 - ITextFont2::GetScaling
 - tom/ITextFont2::GetScaling
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
 - ITextFont2.GetScaling
---

# ITextFont2::GetScaling


## -description

Gets the font horizontal scaling percentage.

## -parameters

### -param pValue [out, retval]

Type: <b>long*</b>

The scaling percentage.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The font horizontal scaling percentage can range from 200, which doubles the widths of characters, to 0, where no scaling is performed.  When the percentage is increased the height does not change.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextfont2-setscaling">ITextFont2::SetScaling</a>