---
UID: NF:tom.ITextDocument2.GetMainStory
title: ITextDocument2::GetMainStory
author: windows-sdk-content
description: Gets the main story.
old-location: controls\itextdocument2_getmainstory.htm
tech.root: controls
ms.assetid: 732165f2-e6cd-4f39-85c6-06faebfa65e2
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: GetMainStory, GetMainStory method [Windows Controls], GetMainStory method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetMainStory method, ITextDocument2.GetMainStory, ITextDocument2::GetMainStory, controls.itextdocument2_getmainstory, tom/ITextDocument2::GetMainStory
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
 - ITextDocument2.GetMainStory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextDocument2::GetMainStory


## -description


Gets the main story.


## -parameters




### -param ppStory [out, retval]

Type: <b><a href="https://msdn.microsoft.com/8b52c6e8-c250-4cfb-979e-770df9f94010">ITextStory</a>**</b>

The main story.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A rich edit control automatically includes the main story; a call to the <a href="https://msdn.microsoft.com/4d6ef859-150b-41e7-be58-b9c87c61f7d8">ITextDocument2::GetNewStory</a> method is not required.




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>
 

 

