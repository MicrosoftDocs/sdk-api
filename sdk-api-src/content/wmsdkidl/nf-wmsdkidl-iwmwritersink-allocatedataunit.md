---
UID: NF:wmsdkidl.IWMWriterSink.AllocateDataUnit
title: IWMWriterSink::AllocateDataUnit (wmsdkidl.h)
description: The AllocateDataUnit method is called by the writer object when it needs a buffer to deliver a data unit.helpviewer_keywords: ["AllocateDataUnit","AllocateDataUnit method [windows Media Format]","AllocateDataUnit method [windows Media Format]","IWMWriterSink interface","IWMWriterSink interface [windows Media Format]","AllocateDataUnit method","IWMWriterSink.AllocateDataUnit","IWMWriterSink::AllocateDataUnit","IWMWriterSinkAllocateDataUnit","wmformat.iwmwritersink_allocatedataunit","wmsdkidl/IWMWriterSink::AllocateDataUnit"]
old-location: wmformat\iwmwritersink_allocatedataunit.htm
tech.root: wmformat
ms.assetid: 56a16163-84e7-4235-8bf3-03e81696bb63
ms.date: 12/05/2018
ms.keywords: AllocateDataUnit, AllocateDataUnit method [windows Media Format], AllocateDataUnit method [windows Media Format],IWMWriterSink interface, IWMWriterSink interface [windows Media Format],AllocateDataUnit method, IWMWriterSink.AllocateDataUnit, IWMWriterSink::AllocateDataUnit, IWMWriterSinkAllocateDataUnit, wmformat.iwmwritersink_allocatedataunit, wmsdkidl/IWMWriterSink::AllocateDataUnit
f1_keywords:
- wmsdkidl/IWMWriterSink.AllocateDataUnit
dev_langs:
- c++
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMWriterSink::AllocateDataUnit


## -description



The <b>AllocateDataUnit</b> method is called by the writer object when it needs a buffer to deliver a data unit. Your implementation of this method returns a buffer of at least the size passed in. You can manage buffers internally in any way that you like. The simplest method is to create a new buffer object for each call, but doing so is quite inefficient. Instead, most sinks maintain several buffers that are reused.




## -parameters




### -param cbDataUnit [in]

Size of the data unit that the writer needs to deliver, in bytes. The buffer you assign to <i>ppDataUnit</i> must be this size or bigger.


### -param ppDataUnit [out]

On return, set to a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer</a> interface of a buffer object.


## -returns



This method is implemented by the application. It should always return S_OK.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink">IWMWriterSink Interface</a>
 

 

