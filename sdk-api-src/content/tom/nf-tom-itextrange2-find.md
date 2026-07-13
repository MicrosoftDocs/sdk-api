---
UID: NF:tom.ITextRange2.Find
title: ITextRange2::Find (tom.h)
description: Searches for math inline functions in text as specified by a source range.
helpviewer_keywords: ["Find","Find method [Windows Controls]","Find method [Windows Controls]","ITextRange2 interface","ITextRange2 interface [Windows Controls]","Find method","ITextRange2.Find","ITextRange2::Find","controls.itextrange2_find","tom/ITextRange2::Find"]
old-location: controls\itextrange2_find.htm
tech.root: Controls
ms.assetid: 4935d322-016a-4c08-858e-42009a9f59f1
ms.date: 12/05/2018
ms.keywords: Find, Find method [Windows Controls], Find method [Windows Controls],ITextRange2 interface, ITextRange2 interface [Windows Controls],Find method, ITextRange2.Find, ITextRange2::Find, controls.itextrange2_find, tom/ITextRange2::Find
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
 - ITextRange2::Find
 - tom/ITextRange2::Find
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
 - ITextRange2.Find
---

# ITextRange2::Find


## -description

Searches for math inline functions in text as specified by a source range.

## -parameters

### -param pRange [in]

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>*</b>

The formatted text to find in the range's text.

### -param Count [in]

Type: <b>long</b>

The number of characters to search through.

### -param Flags [in]

Type: <b>long</b>

Flags that control the search as defined for <a href="/windows/desktop/api/tom/nf-tom-itextrange-findtext">ITextRange::FindText</a>.

### -param pDelta [out]

Type: <b>long*</b>

A count of the number of characters bypassed.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the string is found, and the math inline functions, if any, are the same as their counterparts in the source range, the range limits are changed to be those of the matched string and length is set equal to the length of the string. 

If the string isn't found, the range remains unchanged and length is set equal to 0.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>