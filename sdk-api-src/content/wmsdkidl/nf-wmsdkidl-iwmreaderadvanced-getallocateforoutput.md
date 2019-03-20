---
UID: NF:wmsdkidl.IWMReaderAdvanced.GetAllocateForOutput
title: IWMReaderAdvanced::GetAllocateForOutput (wmsdkidl.h)
author: windows-sdk-content
description: The GetAllocateForOutput method ascertains whether the reader is configured to use the IWMReaderCallbackAdvanced interface to allocate samples delivered by the IWMReaderCallback::OnSample callback.
old-location: wmformat\iwmreaderadvanced_getallocateforoutput.htm
tech.root: wmformat
ms.assetid: b0da74ff-37d9-4bb3-85f2-f8e1585c2d7f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetAllocateForOutput, GetAllocateForOutput method [windows Media Format], GetAllocateForOutput method [windows Media Format],IWMReaderAdvanced interface, IWMReaderAdvanced interface [windows Media Format],GetAllocateForOutput method, IWMReaderAdvanced.GetAllocateForOutput, IWMReaderAdvanced::GetAllocateForOutput, IWMReaderAdvancedGetAllocateForOutput, wmformat.iwmreaderadvanced_getallocateforoutput, wmsdkidl/IWMReaderAdvanced::GetAllocateForOutput
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
 - IWMReaderAdvanced.GetAllocateForOutput
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderAdvanced::GetAllocateForOutput


## -description



The <b>GetAllocateForOutput</b> method ascertains whether the reader is configured to use the <a href="https://msdn.microsoft.com/en-us/library/Dd743494(v=VS.85).aspx">IWMReaderCallbackAdvanced</a> interface to allocate samples delivered by the <a href="https://msdn.microsoft.com/en-us/library/Dd743503(v=VS.85).aspx">IWMReaderCallback::OnSample</a> callback.




## -parameters




### -param dwOutputNum [in]

<b>DWORD</b> containing the identifying number of the output media stream.


### -param pfAllocate [out]

Pointer to a Boolean value that is set to True if the reader uses <b>IWMReaderCallbackAdvanced</b> to allocate samples.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd757429(v=VS.85).aspx">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743481(v=VS.85).aspx">IWMReaderAdvanced::SetAllocateForOutput</a>
 

 

