---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

