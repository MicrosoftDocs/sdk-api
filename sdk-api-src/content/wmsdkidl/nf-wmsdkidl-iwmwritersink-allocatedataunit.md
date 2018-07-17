---
UID: NF:wmsdkidl.IWMWriterSink.AllocateDataUnit
title: IWMWriterSink::AllocateDataUnit
author: windows-sdk-content
description: The AllocateDataUnit method is called by the writer object when it needs a buffer to deliver a data unit.
old-location: wmformat\iwmwritersink_allocatedataunit.htm
old-project: wmformat
ms.assetid: 56a16163-84e7-4235-8bf3-03e81696bb63
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: AllocateDataUnit, AllocateDataUnit method [windows Media Format], AllocateDataUnit method [windows Media Format],IWMWriterSink interface, IWMWriterSink interface [windows Media Format],AllocateDataUnit method, IWMWriterSink.AllocateDataUnit, IWMWriterSink::AllocateDataUnit, IWMWriterSinkAllocateDataUnit, wmformat.iwmwritersink_allocatedataunit, wmsdkidl/IWMWriterSink::AllocateDataUnit
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WM_AETYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMWriterSink.AllocateDataUnit
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMWriterSink::AllocateDataUnit


## -description



The <b>AllocateDataUnit</b> method is called by the writer object when it needs a buffer to deliver a data unit. Your implementation of this method returns a buffer of at least the size passed in. You can manage buffers internally in any way that you like. The simplest method is to create a new buffer object for each call, but doing so is quite inefficient. Instead, most sinks maintain several buffers that are reused.




## -parameters




### -param cbDataUnit [in]

Size of the data unit that the writer needs to deliver, in bytes. The buffer you assign to <i>ppDataUnit</i> must be this size or bigger.


### -param ppDataUnit [out]

On return, set to a pointer to the <a href="https://msdn.microsoft.com/c47c016a-e7eb-4a2c-b365-5537749db5bc">INSSBuffer</a> interface of a buffer object.


## -returns



This method is implemented by the application. It should always return S_OK.




## -see-also




<a href="https://msdn.microsoft.com/73656814-7fac-4567-abcd-dbb3243fcaa8">IWMWriterSink Interface</a>
 

 

