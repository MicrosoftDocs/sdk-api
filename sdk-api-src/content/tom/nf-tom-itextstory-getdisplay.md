---
UID: NF:tom.ITextStory.GetDisplay
title: ITextStory::GetDisplay
author: windows-sdk-content
description: Gets a new display for a story.
old-location: controls\itextstory_getdisplay.htm
tech.root: controls
ms.assetid: e9ea7fbc-b814-4dbd-ae8a-9e260b56abab
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetDisplay, GetDisplay method [Windows Controls], GetDisplay method [Windows Controls],ITextStory interface, ITextStory interface [Windows Controls],GetDisplay method, ITextStory.GetDisplay, ITextStory::GetDisplay, controls.itextstory_getdisplay, tom/ITextStory::GetDisplay
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
req.idl: Tom.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tom.h
api_name:
 - ITextStory.GetDisplay
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextStory::GetDisplay


## -description


Gets a new display for a story.


## -parameters




### -param ppDisplay [out, retval]

Type: <b>IUnknown**</b>

The <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface for a display.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



A story can be displayed by calling <a href="https://msdn.microsoft.com/fa0177be-2016-4205-b121-921dbdbf5b71">ITextStory::SetActive</a>(<b>tomDisplayActive</b>). The <b>ITextStory::GetDisplay</b> method is included, in case it might be advantageous to have more than one display for a set of <a href="https://msdn.microsoft.com/8b52c6e8-c250-4cfb-979e-770df9f94010">ITextStory</a> interfaces.




## -see-also




<a href="https://msdn.microsoft.com/8b52c6e8-c250-4cfb-979e-770df9f94010">ITextStory</a>
 

 

