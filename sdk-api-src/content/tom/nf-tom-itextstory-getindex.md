---
UID: NF:tom.ITextStory.GetIndex
title: ITextStory::GetIndex
author: windows-sdk-content
description: Gets the index of a story.
old-location: controls\itextstory_getindex.htm
old-project: controls
ms.assetid: ef7f4714-6887-429c-8f65-77c14d55a5c4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetIndex, GetIndex method [Windows Controls], GetIndex method [Windows Controls],ITextStory interface, ITextStory interface [Windows Controls],GetIndex method, ITextStory.GetIndex, ITextStory::GetIndex, controls.itextstory_getindex, tom/ITextStory::GetIndex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tom.h
req.include-header: 
req.redist: 
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
 - ITextStory.GetIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStory::GetIndex


## -description


Gets the index of a story.


## -parameters




### -param pValue [out, retval]

Type: <b>long*</b>

The index.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The index is used with the <a href="https://msdn.microsoft.com/bb1322e9-47b2-4770-b5de-c5eeda70eed1">ITextDocument2:: GetStory</a> method.




## -see-also




<a href="https://msdn.microsoft.com/8b52c6e8-c250-4cfb-979e-770df9f94010">ITextStory</a>
 

 

