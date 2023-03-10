---
UID: NF:tom.ITextFont2.SetUnderlinePositionMode
title: ITextFont2::SetUnderlinePositionMode (tom.h)
description: Sets the underline position mode.
helpviewer_keywords: ["ITextFont2 interface [Windows Controls]","SetUnderlinePositionMode method","ITextFont2.SetUnderlinePositionMode","ITextFont2::SetUnderlinePositionMode","SetUnderlinePositionMode","SetUnderlinePositionMode method [Windows Controls]","SetUnderlinePositionMode method [Windows Controls]","ITextFont2 interface","controls.itextfont2_setunderlinepositionmode","tom/ITextFont2::SetUnderlinePositionMode"]
old-location: controls\itextfont2_setunderlinepositionmode.htm
tech.root: Controls
ms.assetid: 31dff2d0-7165-42f0-b3d0-9cb679c738c3
ms.date: 12/05/2018
ms.keywords: ITextFont2 interface [Windows Controls],SetUnderlinePositionMode method, ITextFont2.SetUnderlinePositionMode, ITextFont2::SetUnderlinePositionMode, SetUnderlinePositionMode, SetUnderlinePositionMode method [Windows Controls], SetUnderlinePositionMode method [Windows Controls],ITextFont2 interface, controls.itextfont2_setunderlinepositionmode, tom/ITextFont2::SetUnderlinePositionMode
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
 - ITextFont2::SetUnderlinePositionMode
 - tom/ITextFont2::SetUnderlinePositionMode
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
 - ITextFont2.SetUnderlinePositionMode
---

# ITextFont2::SetUnderlinePositionMode


## -description

Sets the underline position mode.

## -parameters

### -param Value [in]

Type: <b>long</b>

The new underline position mode. It can be one of the following values.<ul>
<li><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomUnderlinePositionAuto</a> (the default)</li>
<li><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomUnderlinePositionBelow</a></li>
<li><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomUnderlinePositionAbove</a></li>
</ul>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextfont2-getunderlinepositionmode">ITextFont2::GetUnderlinePositionMode</a>