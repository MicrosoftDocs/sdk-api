---
UID: NF:tom.ITextDocument2.GetSelection2
title: ITextDocument2::GetSelection2 (tom.h)
description: Gets the active selection. (ITextDocument2.GetSelection2)
helpviewer_keywords: ["GetSelection2","GetSelection2 method [Windows Controls]","GetSelection2 method [Windows Controls]","ITextDocument2 interface","ITextDocument2 interface [Windows Controls]","GetSelection2 method","ITextDocument2.GetSelection2","ITextDocument2::GetSelection2","controls.itextdocument2_getselection2","tom/ITextDocument2::GetSelection2"]
old-location: controls\itextdocument2_getselection2.htm
tech.root: Controls
ms.assetid: a81fde9e-aef8-49cf-88b2-d0416195d70a
ms.date: 12/05/2018
ms.keywords: GetSelection2, GetSelection2 method [Windows Controls], GetSelection2 method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetSelection2 method, ITextDocument2.GetSelection2, ITextDocument2::GetSelection2, controls.itextdocument2_getselection2, tom/ITextDocument2::GetSelection2
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
 - ITextDocument2::GetSelection2
 - tom/ITextDocument2::GetSelection2
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
 - ITextDocument2.GetSelection2
---

# ITextDocument2::GetSelection2


## -description

Gets the active selection.

## -parameters

### -param ppSel [out, retval]

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextselection2">ITextSelection2</a>**</b>

The active selection. This parameter is <b>NULL</b> if the rich edit control is not in-place active.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>
