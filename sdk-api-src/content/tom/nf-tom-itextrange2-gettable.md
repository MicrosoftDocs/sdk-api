---
UID: NF:tom.ITextRange2.GetTable
title: ITextRange2::GetTable (tom.h)
description: Gets the table properties in the currently selected table.
helpviewer_keywords: ["GetTable","GetTable method [Windows Controls]","GetTable method [Windows Controls]","ITextRange2 interface","ITextRange2 interface [Windows Controls]","GetTable method","ITextRange2.GetTable","ITextRange2::GetTable","controls.itextrange2_gettable","tom/ITextRange2::GetTable"]
old-location: controls\itextrange2_gettable.htm
tech.root: Controls
ms.assetid: ade77edf-6a9e-4c8d-a522-3158c802b6dd
ms.date: 12/05/2018
ms.keywords: GetTable, GetTable method [Windows Controls], GetTable method [Windows Controls],ITextRange2 interface, ITextRange2 interface [Windows Controls],GetTable method, ITextRange2.GetTable, ITextRange2::GetTable, controls.itextrange2_gettable, tom/ITextRange2::GetTable
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
 - ITextRange2::GetTable
 - tom/ITextRange2::GetTable
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
 - ITextRange2.GetTable
---

# ITextRange2::GetTable


## -description

Not implemented.

Gets the table properties in the currently selected table.

## -parameters

### -param ppTable [out, retval]

Type: <b>IUnknown**</b>

The table properties.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To select the table when the insertion point is inside a table, call <a href="/windows/desktop/api/tom/nf-tom-itextrange-expand">ITextRange::Expand</a>(tomTable). 

Note: this method isn't implemented in RichEdit (see <a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a> for table functionality).

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>