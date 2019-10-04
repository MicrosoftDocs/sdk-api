---
UID: NF:wmsdkidl.IWMReaderAdvanced.GetAllocateForOutput
title: IWMReaderAdvanced::GetAllocateForOutput (wmsdkidl.h)
author: windows-sdk-content
description: The GetAllocateForOutput method ascertains whether the reader is configured to use the IWMReaderCallbackAdvanced interface to allocate samples delivered by the IWMReaderCallback::OnSample callback.
old-location: wmformat\iwmreaderadvanced_getallocateforoutput.htm
tech.root: wmformat
ms.assetid: b0da74ff-37d9-4bb3-85f2-f8e1585c2d7f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetAllocateForOutput, GetAllocateForOutput method [windows Media Format], GetAllocateForOutput method [windows Media Format],IWMReaderAdvanced interface, IWMReaderAdvanced interface [windows Media Format],GetAllocateForOutput method, IWMReaderAdvanced.GetAllocateForOutput, IWMReaderAdvanced::GetAllocateForOutput, IWMReaderAdvancedGetAllocateForOutput, wmformat.iwmreaderadvanced_getallocateforoutput, wmsdkidl/IWMReaderAdvanced::GetAllocateForOutput
ms.topic: method
f1_keywords: 
 - "wmsdkidl/IWMReaderAdvanced.GetAllocateForOutput"
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
 - IWMReaderAdvanced.GetAllocateForOutput
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderAdvanced::GetAllocateForOutput


## -description



The <b>GetAllocateForOutput</b> method ascertains whether the reader is configured to use the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced">IWMReaderCallbackAdvanced</a> interface to allocate samples delivered by the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample">IWMReaderCallback::OnSample</a> callback.




## -parameters




### -param dwOutputNum [in]

<b>DWORD</b> containing the identifying number of the output media stream.


### -param pfAllocate [out]

Pointer to a Boolean value that is set to True if the reader uses <b>IWMReaderCallbackAdvanced</b> to allocate samples.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced">IWMReaderAdvanced Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforoutput">IWMReaderAdvanced::SetAllocateForOutput</a>
 

 

