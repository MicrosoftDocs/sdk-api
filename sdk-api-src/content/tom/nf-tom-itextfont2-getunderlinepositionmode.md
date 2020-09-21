---
UID: NF:tom.ITextFont2.GetUnderlinePositionMode
title: ITextFont2::GetUnderlinePositionMode (tom.h)
description: Gets the underline position mode.
helpviewer_keywords: ["GetUnderlinePositionMode","GetUnderlinePositionMode method [Windows Controls]","GetUnderlinePositionMode method [Windows Controls]","ITextFont2 interface","ITextFont2 interface [Windows Controls]","GetUnderlinePositionMode method","ITextFont2.GetUnderlinePositionMode","ITextFont2::GetUnderlinePositionMode","controls.itextfont2_getunderlinepositionmode","tom/ITextFont2::GetUnderlinePositionMode"]
old-location: controls\itextfont2_getunderlinepositionmode.htm
tech.root: Controls
ms.assetid: cd7a45be-05b0-4a43-90c8-0fd8393794c0
ms.date: 12/05/2018
ms.keywords: GetUnderlinePositionMode, GetUnderlinePositionMode method [Windows Controls], GetUnderlinePositionMode method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetUnderlinePositionMode method, ITextFont2.GetUnderlinePositionMode, ITextFont2::GetUnderlinePositionMode, controls.itextfont2_getunderlinepositionmode, tom/ITextFont2::GetUnderlinePositionMode
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
 - ITextFont2::GetUnderlinePositionMode
 - tom/ITextFont2::GetUnderlinePositionMode
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
 - ITextFont2.GetUnderlinePositionMode
---

# ITextFont2::GetUnderlinePositionMode


## -description

Gets the underline position mode.

## -parameters

### -param pValue [out, retval]

Type: <b>long*</b>

The underline position mode. It can be one of the following values.

<a href="/windows/win32/api/tom/ne-tom-tomconstants">tomUnderlinePositionAuto</a>
<a href="/windows/win32/api/tom/ne-tom-tomconstants">tomUnderlinePositionBelow</a>
<a href="/windows/win32/api/tom/ne-tom-tomconstants">tomUnderlinePositionAbove</a>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextfont2-setunderlinepositionmode">ITextFont2::SetUnderlinePositionMode</a>