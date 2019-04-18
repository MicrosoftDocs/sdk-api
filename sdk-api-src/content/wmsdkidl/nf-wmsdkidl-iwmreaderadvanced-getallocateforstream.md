---
UID: NF:wmsdkidl.IWMReaderAdvanced.GetAllocateForStream
title: IWMReaderAdvanced::GetAllocateForStream (wmsdkidl.h)
author: windows-sdk-content
description: The GetAllocateForStream method ascertains whether the reader is configured to use IWMReaderCallbackAdvanced to allocate stream samples delivered by the IWMReaderCallbackAdvanced::OnStreamSample callback.
old-location: wmformat\iwmreaderadvanced_getallocateforstream.htm
tech.root: wmformat
ms.assetid: 816f13b1-9856-482d-b5b1-4aaf5c61c230
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetAllocateForStream, GetAllocateForStream method [windows Media Format], GetAllocateForStream method [windows Media Format],IWMReaderAdvanced interface, IWMReaderAdvanced interface [windows Media Format],GetAllocateForStream method, IWMReaderAdvanced.GetAllocateForStream, IWMReaderAdvanced::GetAllocateForStream, IWMReaderAdvancedGetAllocateForStream, wmformat.iwmreaderadvanced_getallocateforstream, wmsdkidl/IWMReaderAdvanced::GetAllocateForStream
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
 - IWMReaderAdvanced.GetAllocateForStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderAdvanced::GetAllocateForStream


## -description



The <b>GetAllocateForStream</b> method ascertains whether the reader is configured to use <a href="https://msdn.microsoft.com/en-us/library/Dd743494(v=VS.85).aspx">IWMReaderCallbackAdvanced</a> to allocate stream samples delivered by the <a href="https://msdn.microsoft.com/en-us/library/Dd743500(v=VS.85).aspx">IWMReaderCallbackAdvanced::OnStreamSample</a> callback.




## -parameters




### -param dwSreamNum [in]

<b>WORD</b> containing the stream number.


### -param pfAllocate [out]

Pointer to a Boolean value that is set to True if the reader uses <b>IWMReaderCallbackAdvanced</b> to allocate samples.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



Stream numbers are in the range of 1 through 63.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd757429(v=VS.85).aspx">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743482(v=VS.85).aspx">IWMReaderAdvanced::SetAllocateForStream</a>
 

 

