---
UID: NF:wmsdkidl.IWMReaderAdvanced3.StopNetStreaming
title: IWMReaderAdvanced3::StopNetStreaming (wmsdkidl.h)
author: windows-sdk-content
description: The StopNetStreaming method halts network streaming. Any samples that have already been received from the network are delivered as usual.
old-location: wmformat\iwmreaderadvanced3_stopnetstreaming.htm
tech.root: wmformat
ms.assetid: e323f967-02d5-4472-a9b3-cb8a2b80070e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMReaderAdvanced3 interface [windows Media Format],StopNetStreaming method, IWMReaderAdvanced3.StopNetStreaming, IWMReaderAdvanced3::StopNetStreaming, IWMReaderAdvanced3StopNetStreaming, StopNetStreaming, StopNetStreaming method [windows Media Format], StopNetStreaming method [windows Media Format],IWMReaderAdvanced3 interface, wmformat.iwmreaderadvanced3_stopnetstreaming, wmsdkidl/IWMReaderAdvanced3::StopNetStreaming
ms.topic: method
f1_keywords: ["wmsdkidl/IWMReaderAdvanced3.StopNetStreaming"]
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
 - IWMReaderAdvanced3.StopNetStreaming
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderAdvanced3::StopNetStreaming


## -description



The <b>StopNetStreaming</b> method halts network streaming. Any samples that have already been received from the network are delivered as usual.




## -parameters






## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



When this method is finished, a WMT_END_OF_STREAMING message will be delivered to the <b>OnStatus</b> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3">IWMReaderAdvanced3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus">IWMStatusCallback::OnStatus</a>
 

 

