---
UID: NF:tom.ITextDocument2.Range2
title: ITextDocument2::Range2 (tom.h)
description: Retrieves a new text range for the active story of the document.
helpviewer_keywords: ["ITextDocument2 interface [Windows Controls]","Range2 method","ITextDocument2.Range2","ITextDocument2::Range2","Range2","Range2 method [Windows Controls]","Range2 method [Windows Controls]","ITextDocument2 interface","controls.itextdocument2_range2","tom/ITextDocument2::Range2"]
old-location: controls\itextdocument2_range2.htm
tech.root: Controls
ms.assetid: e0cd3788-de0e-4b57-8f24-f0897e2b0bed
ms.date: 12/05/2018
ms.keywords: ITextDocument2 interface [Windows Controls],Range2 method, ITextDocument2.Range2, ITextDocument2::Range2, Range2, Range2 method [Windows Controls], Range2 method [Windows Controls],ITextDocument2 interface, controls.itextdocument2_range2, tom/ITextDocument2::Range2
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
 - ITextDocument2::Range2
 - tom/ITextDocument2::Range2
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
 - ITextDocument2.Range2
---

# ITextDocument2::Range2


## -description

Retrieves a new text range for the active story of the document.

## -parameters

### -param cpActive [in]

Type: <b>long</b>

The active end of the new text range. The default value is 0; that is, the beginning of the story.

### -param cpAnchor [in]

Type: <b>long</b>

The anchor end of the new text range. The default value is 0.

### -param ppRange [out, retval]

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>**</b>

The new text range.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>