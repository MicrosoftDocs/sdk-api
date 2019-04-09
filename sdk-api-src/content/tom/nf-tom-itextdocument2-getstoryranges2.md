---
UID: NF:tom.ITextDocument2.GetStoryRanges2
title: ITextDocument2::GetStoryRanges2 (tom.h)
author: windows-sdk-content
description: Gets an object for enumerating the stories in a document.
old-location: controls\itextdocument2_getstoryranges2.htm
tech.root: Controls
ms.assetid: ec62db67-d5e6-47d9-ad35-0fc33ba45b6b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetStoryRanges2, GetStoryRanges2 method [Windows Controls], GetStoryRanges2 method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetStoryRanges2 method, ITextDocument2.GetStoryRanges2, ITextDocument2::GetStoryRanges2, controls.itextdocument2_getstoryranges2, tom/ITextDocument2::GetStoryRanges2
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
req.lib: 
req.dll: Msftedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextDocument2.GetStoryRanges2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextDocument2::GetStoryRanges2


## -description


Gets an object for enumerating the stories in a document. 


## -parameters




### -param ppStories [out, retval]

Type: <b><a href="https://msdn.microsoft.com/24e2dd79-8054-44e3-aa68-778a96e2f66a">ITextStoryRanges2</a>**</b>

The object for enumerating stories.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



Call this method only if the <a href="https://msdn.microsoft.com/en-us/library/Bb774027(v=VS.85).aspx">ITextDocument::GetStoryCount</a> method returns a value that is greater than one.




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>
 

 

