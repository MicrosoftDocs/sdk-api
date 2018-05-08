---
UID: NF:tom.ITextStoryRanges2.Item2
title: ITextStoryRanges2::Item2
author: windows-driver-content
description: Gets an ITextRange2 object for a story, by index, in a stories collection.
old-location: controls\itextstoryranges2_item2.htm
old-project: Controls
ms.assetid: 0e77584e-e7ea-44ee-bce8-6f3b84d106bb
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: ITextStoryRanges2 interface [Windows Controls],Item2 method, ITextStoryRanges2.Item2, ITextStoryRanges2::Item2, Item2, Item2 method [Windows Controls], Item2 method [Windows Controls],ITextStoryRanges2 interface, controls.itextstoryranges2_item2, tom/ITextStoryRanges2::Item2
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MANCODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextStoryRanges2.Item2
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

