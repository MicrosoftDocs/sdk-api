---
UID: NF:wmsdkidl.IWMReaderAdvanced3.StopNetStreaming
title: IWMReaderAdvanced3::StopNetStreaming method
author: windows-driver-content
description: The StopNetStreaming method halts network streaming. Any samples that have already been received from the network are delivered as usual.
old-location: wmformat\iwmreaderadvanced3_stopnetstreaming.htm
old-project: wmformat
ms.assetid: e323f967-02d5-4472-a9b3-cb8a2b80070e
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IWMReaderAdvanced3, IWMReaderAdvanced3 interface [windows Media Format], StopNetStreaming method, IWMReaderAdvanced3::StopNetStreaming, IWMReaderAdvanced3StopNetStreaming, StopNetStreaming method [windows Media Format], StopNetStreaming method [windows Media Format], IWMReaderAdvanced3 interface, StopNetStreaming,IWMReaderAdvanced3.StopNetStreaming, wmformat.iwmreaderadvanced3_stopnetstreaming, wmsdkidl/IWMReaderAdvanced3::StopNetStreaming
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmvcore.lib
-	Wmvcore.dll
-	WMStubDRM.lib
-	WMStubDRM.dll
api_name:
-	IWMReaderAdvanced3.StopNetStreaming
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderAdvanced3::StopNetStreaming method


## -description



The <b>StopNetStreaming</b> method halts network streaming. Any samples that have already been received from the network are delivered as usual.




## -parameters






## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



When this method is finished, a WMT_END_OF_STREAMING message will be delivered to the <b>OnStatus</b> method.




## -see-also




<a href="https://msdn.microsoft.com/20bf3c00-0f35-4b8e-b78d-a36fbfd865b7">IWMReaderAdvanced3 Interface</a>



<a href="https://msdn.microsoft.com/7b8cdb21-96e1-4cf9-8422-72bce693afb1">IWMStatusCallback::OnStatus</a>
 

 

