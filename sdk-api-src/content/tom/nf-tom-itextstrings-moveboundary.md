---
UID: NF:tom.ITextStrings.MoveBoundary
title: ITextStrings::MoveBoundary (tom.h)
description: Moves the start boundary of a string, by index, for a selected number of characters.
helpviewer_keywords: ["ITextStrings interface [Windows Controls]","MoveBoundary method","ITextStrings.MoveBoundary","ITextStrings::MoveBoundary","MoveBoundary","MoveBoundary method [Windows Controls]","MoveBoundary method [Windows Controls]","ITextStrings interface","controls.itextstrings_moveboundary","tom/ITextStrings::MoveBoundary"]
old-location: controls\itextstrings_moveboundary.htm
tech.root: Controls
ms.assetid: db0eff33-f20a-481e-bcae-8a72674ab906
ms.date: 12/05/2018
ms.keywords: ITextStrings interface [Windows Controls],MoveBoundary method, ITextStrings.MoveBoundary, ITextStrings::MoveBoundary, MoveBoundary, MoveBoundary method [Windows Controls], MoveBoundary method [Windows Controls],ITextStrings interface, controls.itextstrings_moveboundary, tom/ITextStrings::MoveBoundary
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
 - ITextStrings::MoveBoundary
 - tom/ITextStrings::MoveBoundary
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
 - ITextStrings.MoveBoundary
---

# ITextStrings::MoveBoundary


## -description

Moves the start boundary of a string, by index, for a selected number of characters.

## -parameters

### -param iString [in]

Type: <b>long</b>

The string index.

### -param cch [in]

Type: <b>long</b>

The selected number of characters to move the boundary.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The index is relative to the top of the collection, so <i>iString</i> = 0 moves the top string boundary, <i>iString</i> = –1 moves the boundary of the string below the top string, and so on.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextstrings">ITextStrings</a>