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

# ITextStoryRanges2::Item2


## -description


Gets an <a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a> object for a story, by index, in a stories collection.


## -parameters




### -param Index [in]

Type: <b>long</b>

The index of the story range. The default value is 1.


### -param ppRange [out, retval]

Type: <b>ITextRange2**</b>

The range.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The first story has an index of 1, and the last story  has an index equal to the count  retrieved by the <a href="https://msdn.microsoft.com/ef7f5b30-c3d1-4b8f-ad2d-925e09cab462">ITextStoryRanges::GetCount</a> method. Negative index values count from the last story to the first; that is, an index of –1 gets the last story in the collection, and an index of –<i>count</i> gets the first story.




## -see-also




<a href="https://msdn.microsoft.com/24e2dd79-8054-44e3-aa68-778a96e2f66a">ITextStoryRanges2</a>
 

 

