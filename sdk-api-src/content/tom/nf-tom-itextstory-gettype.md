---
UID: NF:tom.ITextStory.GetType
title: ITextStory::GetType
author: windows-sdk-content
description: Gets this story's type.
old-location: controls\itextstory_gettype.htm
old-project: Controls
ms.assetid: 43a75284-c461-4118-834c-9ce5ded55094
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetType, GetType method [Windows Controls], GetType method [Windows Controls],ITextStory interface, ITextStory interface [Windows Controls],GetType method, ITextStory.GetType, ITextStory::GetType, controls.itextstory_gettype, tom/ITextStory::GetType, tomCommentsStory, tomEndnotesStory, tomEvenPagesFooterStory, tomEvenPagesHeaderStory, tomFindStory, tomFirstPageFooterStory, tomFirstPageHeaderStory, tomFootnotesStory, tomMainTextStory, tomPrimaryFooterStory, tomPrimaryHeaderStory, tomReplaceStory, tomScratchStory, tomTextFrameStory, tomUnknownStory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MANCODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tom.h
api_name:
 - ITextStory.GetType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/8b52c6e8-c250-4cfb-979e-770df9f94010">ITextStory</a>



<a href="https://msdn.microsoft.com/43a75284-c461-4118-834c-9ce5ded55094">ITextStory::SetType</a>
 

 

