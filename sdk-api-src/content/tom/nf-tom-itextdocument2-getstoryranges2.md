---
UID: NF:tom.ITextDocument2.GetStoryRanges2
title: ITextDocument2::GetStoryRanges2 (tom.h)
description: Gets an object for enumerating the stories in a document.
helpviewer_keywords: ["GetStoryRanges2","GetStoryRanges2 method [Windows Controls]","GetStoryRanges2 method [Windows Controls]","ITextDocument2 interface","ITextDocument2 interface [Windows Controls]","GetStoryRanges2 method","ITextDocument2.GetStoryRanges2","ITextDocument2::GetStoryRanges2","controls.itextdocument2_getstoryranges2","tom/ITextDocument2::GetStoryRanges2"]
old-location: controls\itextdocument2_getstoryranges2.htm
tech.root: Controls
ms.assetid: ec62db67-d5e6-47d9-ad35-0fc33ba45b6b
ms.date: 12/05/2018
ms.keywords: GetStoryRanges2, GetStoryRanges2 method [Windows Controls], GetStoryRanges2 method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetStoryRanges2 method, ITextDocument2.GetStoryRanges2, ITextDocument2::GetStoryRanges2, controls.itextdocument2_getstoryranges2, tom/ITextDocument2::GetStoryRanges2
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
 - ITextDocument2::GetStoryRanges2
 - tom/ITextDocument2::GetStoryRanges2
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
 - ITextDocument2.GetStoryRanges2
---

# ITextDocument2::GetStoryRanges2


## -description

Gets an object for enumerating the stories in a document.

## -parameters

### -param ppStories [out, retval]

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextstoryranges2">ITextStoryRanges2</a>**</b>

The object for enumerating stories.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Call this method only if the <a href="/windows/desktop/api/tom/nf-tom-itextdocument-getstorycount">ITextDocument::GetStoryCount</a> method returns a value that is greater than one.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>