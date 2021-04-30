---
UID: NF:tom.ITextStory.GetIndex
title: ITextStory::GetIndex (tom.h)
description: Gets the index of a story.
helpviewer_keywords: ["GetIndex","GetIndex method [Windows Controls]","GetIndex method [Windows Controls]","ITextStory interface","ITextStory interface [Windows Controls]","GetIndex method","ITextStory.GetIndex","ITextStory::GetIndex","controls.itextstory_getindex","tom/ITextStory::GetIndex"]
old-location: controls\itextstory_getindex.htm
tech.root: Controls
ms.assetid: ef7f4714-6887-429c-8f65-77c14d55a5c4
ms.date: 12/05/2018
ms.keywords: GetIndex, GetIndex method [Windows Controls], GetIndex method [Windows Controls],ITextStory interface, ITextStory interface [Windows Controls],GetIndex method, ITextStory.GetIndex, ITextStory::GetIndex, controls.itextstory_getindex, tom/ITextStory::GetIndex
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tom.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextStory::GetIndex
 - tom/ITextStory::GetIndex
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tom.h
api_name:
 - ITextStory.GetIndex
---

# ITextStory::GetIndex


## -description

Gets the index of a story.

## -parameters

### -param pValue [out, retval]

Type: <b>long*</b>

The index.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The index is used with the <a href="/windows/desktop/api/tom/nf-tom-itextdocument2-getstory">ITextDocument2:: GetStory</a> method.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextstory">ITextStory</a>