---
UID: NF:tom.ITextDocument2.RangeFromPoint2
title: ITextDocument2::RangeFromPoint2 (tom.h)
description: Retrieves the degenerate range at (or nearest to) a particular point on the screen.
helpviewer_keywords: ["ITextDocument2 interface [Windows Controls]","RangeFromPoint2 method","ITextDocument2.RangeFromPoint2","ITextDocument2::RangeFromPoint2","RangeFromPoint2","RangeFromPoint2 method [Windows Controls]","RangeFromPoint2 method [Windows Controls]","ITextDocument2 interface","controls.itextdocument2_rangefrompoint2","tom/ITextDocument2::RangeFromPoint2"]
old-location: controls\itextdocument2_rangefrompoint2.htm
tech.root: Controls
ms.assetid: 3212c6cc-a1fb-44ca-aba9-2234414e7a39
ms.date: 12/05/2018
ms.keywords: ITextDocument2 interface [Windows Controls],RangeFromPoint2 method, ITextDocument2.RangeFromPoint2, ITextDocument2::RangeFromPoint2, RangeFromPoint2, RangeFromPoint2 method [Windows Controls], RangeFromPoint2 method [Windows Controls],ITextDocument2 interface, controls.itextdocument2_rangefrompoint2, tom/ITextDocument2::RangeFromPoint2
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
 - ITextDocument2::RangeFromPoint2
 - tom/ITextDocument2::RangeFromPoint2
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
 - ITextDocument2.RangeFromPoint2
---

# ITextDocument2::RangeFromPoint2


## -description

Retrieves the degenerate range at (or nearest to) a particular point on the screen.

## -parameters

### -param x [in]

Type: <b>long</b>

The x-coordinate of a point, in screen coordinates.

### -param y [in]

Type: <b>long</b>

The y-coordinate of a point, in screen coordinates.

### -param Type [in]

Type: <b>long</b>

The alignment type of the specified point. For a list of valid values, see <a href="/windows/desktop/api/tom/nf-tom-itextrange-getpoint">ITextRange::GetPoint</a>.

### -param ppRange [out, retval]

Type: <b>ITextRange2**</b>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>