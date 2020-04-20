---
UID: NF:wmsdkidl.IWMWriterSink.OnDataUnit
title: IWMWriterSink::OnDataUnit (wmsdkidl.h)
description: The OnDataUnit method is called by the writer when a data unit is ready for the sink. How your application handles the data unit depends upon the destination of the content.helpviewer_keywords: ["IWMWriterSink interface [windows Media Format]","OnDataUnit method","IWMWriterSink.OnDataUnit","IWMWriterSink::OnDataUnit","IWMWriterSinkOnDataUnit","OnDataUnit","OnDataUnit method [windows Media Format]","OnDataUnit method [windows Media Format]","IWMWriterSink interface","wmformat.iwmwritersink_ondataunit","wmsdkidl/IWMWriterSink::OnDataUnit"]
old-location: wmformat\iwmwritersink_ondataunit.htm
tech.root: wmformat
ms.assetid: 32e52cdb-e7cb-4caf-a202-0d2ff746017c
ms.date: 12/05/2018
ms.keywords: IWMWriterSink interface [windows Media Format],OnDataUnit method, IWMWriterSink.OnDataUnit, IWMWriterSink::OnDataUnit, IWMWriterSinkOnDataUnit, OnDataUnit, OnDataUnit method [windows Media Format], OnDataUnit method [windows Media Format],IWMWriterSink interface, wmformat.iwmwritersink_ondataunit, wmsdkidl/IWMWriterSink::OnDataUnit
f1_keywords:
- wmsdkidl/IWMWriterSink.OnDataUnit
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
- IWMWriterSink.OnDataUnit
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMWriterSink::OnDataUnit


## -description



The <b>OnDataUnit</b> method is called by the writer when a data unit is ready for the sink. How your application handles the data unit depends upon the destination of the content.




## -parameters




### -param pDataUnit [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer</a> interface on an object containing the data unit.


## -returns



This method is implemented by the application. It should always return S_OK.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink">IWMWriterSink Interface</a>
 

 

