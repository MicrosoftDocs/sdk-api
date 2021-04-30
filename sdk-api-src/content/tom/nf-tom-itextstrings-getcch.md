---
UID: NF:tom.ITextStrings.GetCch
title: ITextStrings::GetCch (tom.h)
description: Gets the count of characters for a selected string index.
helpviewer_keywords: ["GetCch","GetCch method [Windows Controls]","GetCch method [Windows Controls]","ITextStrings interface","ITextStrings interface [Windows Controls]","GetCch method","ITextStrings.GetCch","ITextStrings::GetCch","controls.itextstrings_getcch","tom/ITextStrings::GetCch"]
old-location: controls\itextstrings_getcch.htm
tech.root: Controls
ms.assetid: 73b88019-f74b-4345-95f3-9f924c999b8a
ms.date: 12/05/2018
ms.keywords: GetCch, GetCch method [Windows Controls], GetCch method [Windows Controls],ITextStrings interface, ITextStrings interface [Windows Controls],GetCch method, ITextStrings.GetCch, ITextStrings::GetCch, controls.itextstrings_getcch, tom/ITextStrings::GetCch
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
 - ITextStrings::GetCch
 - tom/ITextStrings::GetCch
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
 - ITextStrings.GetCch
---

# ITextStrings::GetCch


## -description

Gets the count of characters for a selected string index.

## -parameters

### -param iString [in]

Type: <b>long</b>

The string index.

### -param pcch [out]

Type: <b>long*</b>

The string character count.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The index is relative to the top of the collection, so <i>iString</i> = 0 returns the character count of the top string, <i>iString</i> = –1 returns that for the one below the top string, and so on.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextstrings">ITextStrings</a>