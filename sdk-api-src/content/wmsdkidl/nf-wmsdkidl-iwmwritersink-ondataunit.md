---
UID: NF:wmsdkidl.IWMWriterSink.OnDataUnit
title: IWMWriterSink::OnDataUnit
author: windows-sdk-content
description: The OnDataUnit method is called by the writer when a data unit is ready for the sink. How your application handles the data unit depends upon the destination of the content.
old-location: wmformat\iwmwritersink_ondataunit.htm
tech.root: wmformat
ms.assetid: 32e52cdb-e7cb-4caf-a202-0d2ff746017c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMWriterSink interface [windows Media Format],OnDataUnit method, IWMWriterSink.OnDataUnit, IWMWriterSink::OnDataUnit, IWMWriterSinkOnDataUnit, OnDataUnit, OnDataUnit method [windows Media Format], OnDataUnit method [windows Media Format],IWMWriterSink interface, wmformat.iwmwritersink_ondataunit, wmsdkidl/IWMWriterSink::OnDataUnit
ms.prod: windows-hardware
ms.technology: windows-devices
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMWriterSink::OnDataUnit


## -description



The <b>OnDataUnit</b> method is called by the writer when a data unit is ready for the sink. How your application handles the data unit depends upon the destination of the content.




## -parameters




### -param pDataUnit [in]

Pointer to an <a href="https://msdn.microsoft.com/c47c016a-e7eb-4a2c-b365-5537749db5bc">INSSBuffer</a> interface on an object containing the data unit.


## -returns



This method is implemented by the application. It should always return S_OK.




## -see-also




<a href="https://msdn.microsoft.com/73656814-7fac-4567-abcd-dbb3243fcaa8">IWMWriterSink Interface</a>
 

 

