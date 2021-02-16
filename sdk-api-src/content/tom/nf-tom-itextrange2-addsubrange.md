---
UID: NF:tom.ITextRange2.AddSubrange
title: ITextRange2::AddSubrange (tom.h)
description: Adds a subrange to this range.
helpviewer_keywords: ["AddSubrange","AddSubrange method [Windows Controls]","AddSubrange method [Windows Controls]","ITextRange2 interface","ITextRange2 interface [Windows Controls]","AddSubrange method","ITextRange2.AddSubrange","ITextRange2::AddSubrange","controls.itextrange2_addsubrange","tom/ITextRange2::AddSubrange"]
old-location: controls\itextrange2_addsubrange.htm
tech.root: Controls
ms.assetid: ffd1f166-a37c-4b39-9878-a4008260f675
ms.date: 12/05/2018
ms.keywords: AddSubrange, AddSubrange method [Windows Controls], AddSubrange method [Windows Controls],ITextRange2 interface, ITextRange2 interface [Windows Controls],AddSubrange method, ITextRange2.AddSubrange, ITextRange2::AddSubrange, controls.itextrange2_addsubrange, tom/ITextRange2::AddSubrange
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
 - ITextRange2::AddSubrange
 - tom/ITextRange2::AddSubrange
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
 - ITextRange2.AddSubrange
---

# ITextRange2::AddSubrange


## -description

Adds a subrange to this range.

## -parameters

### -param cp1 [in]

Type: <b>long</b>

The active-end character position of the subrange.

### -param cp2 [in]

Type: <b>long</b>

The anchor-end character position  of the subrange.

### -param Activate [in]

Type: <b>long</b>

The activate parameter.  If this parameter is <b>tomTrue</b>, the new subrange is the active subrange, with <i>cp1</i> as the active end, and <i>cp2</i> the anchor end.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>