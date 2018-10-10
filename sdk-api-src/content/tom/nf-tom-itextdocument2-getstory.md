---
UID: NF:tom.ITextDocument2.GetStory
title: ITextDocument2::GetStory
author: windows-sdk-content
description: Retrieves the story that corresponds to a particular index.
old-location: controls\itextdocument2_getstory.htm
tech.root: Controls
ms.assetid: bb1322e9-47b2-4770-b5de-c5eeda70eed1
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: GetStory, GetStory method [Windows Controls], GetStory method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetStory method, ITextDocument2.GetStory, ITextDocument2::GetStory, controls.itextdocument2_getstory, tom/ITextDocument2::GetStory
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
 - ITextDocument2.GetStory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextDocument2::GetStory


## -description


Retrieves the story that corresponds to a particular index.


## -parameters




### -param Index [in]

Type: <b>long</b>

The index of the story to retrieve.


### -param ppStory [out, retval]

Type: <b><a href="https://msdn.microsoft.com/8b52c6e8-c250-4cfb-979e-770df9f94010">ITextStory</a>**</b>

The story.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>
 

 

