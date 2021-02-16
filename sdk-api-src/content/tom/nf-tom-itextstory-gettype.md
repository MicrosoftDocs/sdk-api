---
UID: NF:tom.ITextStory.GetType
title: ITextStory::GetType (tom.h)
description: Gets this story's type.
helpviewer_keywords: ["GetType","GetType method [Windows Controls]","GetType method [Windows Controls]","ITextStory interface","ITextStory interface [Windows Controls]","GetType method","ITextStory.GetType","ITextStory::GetType","controls.itextstory_gettype","tom/ITextStory::GetType","tomCommentsStory","tomEndnotesStory","tomEvenPagesFooterStory","tomEvenPagesHeaderStory","tomFindStory","tomFirstPageFooterStory","tomFirstPageHeaderStory","tomFootnotesStory","tomMainTextStory","tomPrimaryFooterStory","tomPrimaryHeaderStory","tomReplaceStory","tomScratchStory","tomTextFrameStory","tomUnknownStory"]
old-location: controls\itextstory_gettype.htm
tech.root: Controls
ms.assetid: 43a75284-c461-4118-834c-9ce5ded55094
ms.date: 12/05/2018
ms.keywords: GetType, GetType method [Windows Controls], GetType method [Windows Controls],ITextStory interface, ITextStory interface [Windows Controls],GetType method, ITextStory.GetType, ITextStory::GetType, controls.itextstory_gettype, tom/ITextStory::GetType, tomCommentsStory, tomEndnotesStory, tomEvenPagesFooterStory, tomEvenPagesHeaderStory, tomFindStory, tomFirstPageFooterStory, tomFirstPageHeaderStory, tomFootnotesStory, tomMainTextStory, tomPrimaryFooterStory, tomPrimaryHeaderStory, tomReplaceStory, tomScratchStory, tomTextFrameStory, tomUnknownStory
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
 - ITextStory::GetType
 - tom/ITextStory::GetType
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
 - ITextStory.GetType
---

# ITextStory::GetType


## -description

Gets this story's type.

## -parameters

### -param pValue [out, retval]

Type: <b>long*</b>

This story's type. It can be any of the following values, or a custom client value from 100 to 65535.


<a id="tomCommentsStory"></a>
<a id="tomcommentsstory"></a>
<a id="TOMCOMMENTSSTORY"></a>


#### tomCommentsStory

<a id="tomEndnotesStory"></a>
<a id="tomendnotesstory"></a>
<a id="TOMENDNOTESSTORY"></a>


#### tomEndnotesStory

<a id="tomEvenPagesFooterStory"></a>
<a id="tomevenpagesfooterstory"></a>
<a id="TOMEVENPAGESFOOTERSTORY"></a>


#### tomEvenPagesFooterStory

<a id="tomEvenPagesHeaderStory"></a>
<a id="tomevenpagesheaderstory"></a>
<a id="TOMEVENPAGESHEADERSTORY"></a>


#### tomEvenPagesHeaderStory

<a id="tomFindStory"></a>
<a id="tomfindstory"></a>
<a id="TOMFINDSTORY"></a>


#### tomFindStory

<a id="tomFirstPageFooterStory"></a>
<a id="tomfirstpagefooterstory"></a>
<a id="TOMFIRSTPAGEFOOTERSTORY"></a>


#### tomFirstPageFooterStory

<a id="tomFirstPageHeaderStory"></a>
<a id="tomfirstpageheaderstory"></a>
<a id="TOMFIRSTPAGEHEADERSTORY"></a>


#### tomFirstPageHeaderStory

<a id="tomFootnotesStory"></a>
<a id="tomfootnotesstory"></a>
<a id="TOMFOOTNOTESSTORY"></a>


#### tomFootnotesStory

<a id="tomMainTextStory"></a>
<a id="tommaintextstory"></a>
<a id="TOMMAINTEXTSTORY"></a>


#### tomMainTextStory

<a id="tomPrimaryFooterStory"></a>
<a id="tomprimaryfooterstory"></a>
<a id="TOMPRIMARYFOOTERSTORY"></a>


#### tomPrimaryFooterStory

<a id="tomPrimaryHeaderStory"></a>
<a id="tomprimaryheaderstory"></a>
<a id="TOMPRIMARYHEADERSTORY"></a>


#### tomPrimaryHeaderStory

<a id="tomReplaceStory"></a>
<a id="tomreplacestory"></a>
<a id="TOMREPLACESTORY"></a>


#### tomReplaceStory

<a id="tomScratchStory"></a>
<a id="tomscratchstory"></a>
<a id="TOMSCRATCHSTORY"></a>


#### tomScratchStory

<a id="tomTextFrameStory"></a>
<a id="tomtextframestory"></a>
<a id="TOMTEXTFRAMESTORY"></a>


#### tomTextFrameStory

<a id="tomUnknownStory"></a>
<a id="tomunknownstory"></a>
<a id="TOMUNKNOWNSTORY"></a>


#### tomUnknownStory

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextstory">ITextStory</a>



<a href="/windows/desktop/api/tom/nf-tom-itextstory-gettype">ITextStory::SetType</a>