---
UID: NF:tom.ITextStrings.InsertNullStr
title: ITextStrings::InsertNullStr (tom.h)
description: Inserts a NULL string in the collection at a selected string index.
helpviewer_keywords: ["ITextStrings interface [Windows Controls]","InsertNullStr method","ITextStrings.InsertNullStr","ITextStrings::InsertNullStr","InsertNullStr","InsertNullStr method [Windows Controls]","InsertNullStr method [Windows Controls]","ITextStrings interface","controls.itextstrings_insertnullstr","tom/ITextStrings::InsertNullStr"]
old-location: controls\itextstrings_insertnullstr.htm
tech.root: Controls
ms.assetid: dc269f41-f65c-4335-ac5c-5c57187f20aa
ms.date: 12/05/2018
ms.keywords: ITextStrings interface [Windows Controls],InsertNullStr method, ITextStrings.InsertNullStr, ITextStrings::InsertNullStr, InsertNullStr, InsertNullStr method [Windows Controls], InsertNullStr method [Windows Controls],ITextStrings interface, controls.itextstrings_insertnullstr, tom/ITextStrings::InsertNullStr
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
 - ITextStrings::InsertNullStr
 - tom/ITextStrings::InsertNullStr
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
 - ITextStrings.InsertNullStr
---

# ITextStrings::InsertNullStr


## -description

Inserts a <b>NULL</b> string in the collection at a selected string index.

## -parameters

### -param iString [in]

Type: <b>long</b>

The string index.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The index is relative to the top of the collection, so <i>iString</i> = 0 inserts the <b>NULL</b> string at the top, <i>iString</i> = –1 inserts it below the top string, and so on.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextstrings">ITextStrings</a>