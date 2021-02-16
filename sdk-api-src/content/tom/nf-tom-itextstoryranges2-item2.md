---
UID: NF:tom.ITextStoryRanges2.Item2
title: ITextStoryRanges2::Item2 (tom.h)
description: Gets an ITextRange2 object for a story, by index, in a stories collection.
helpviewer_keywords: ["ITextStoryRanges2 interface [Windows Controls]","Item2 method","ITextStoryRanges2.Item2","ITextStoryRanges2::Item2","Item2","Item2 method [Windows Controls]","Item2 method [Windows Controls]","ITextStoryRanges2 interface","controls.itextstoryranges2_item2","tom/ITextStoryRanges2::Item2"]
old-location: controls\itextstoryranges2_item2.htm
tech.root: Controls
ms.assetid: 0e77584e-e7ea-44ee-bce8-6f3b84d106bb
ms.date: 12/05/2018
ms.keywords: ITextStoryRanges2 interface [Windows Controls],Item2 method, ITextStoryRanges2.Item2, ITextStoryRanges2::Item2, Item2, Item2 method [Windows Controls], Item2 method [Windows Controls],ITextStoryRanges2 interface, controls.itextstoryranges2_item2, tom/ITextStoryRanges2::Item2
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
 - ITextStoryRanges2::Item2
 - tom/ITextStoryRanges2::Item2
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
 - ITextStoryRanges2.Item2
---

# ITextStoryRanges2::Item2


## -description

Gets an <a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a> object for a story, by index, in a stories collection.

## -parameters

### -param Index [in]

Type: <b>long</b>

The index of the story range. The default value is 1.

### -param ppRange [out, retval]

Type: <b>ITextRange2**</b>

The range.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The first story has an index of 1, and the last story  has an index equal to the count  retrieved by the <a href="/windows/desktop/api/tom/nf-tom-itextstoryranges-getcount">ITextStoryRanges::GetCount</a> method. Negative index values count from the last story to the first; that is, an index of –1 gets the last story in the collection, and an index of –<i>count</i> gets the first story.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextstoryranges2">ITextStoryRanges2</a>