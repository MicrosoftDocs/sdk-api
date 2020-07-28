---
UID: NF:wmsdkidl.IWMReaderAdvanced.SetAllocateForStream
title: IWMReaderAdvanced::SetAllocateForStream (wmsdkidl.h)
description: The SetAllocateForStream method specifies whether the reader uses IWMReaderCallbackAdvanced::AllocateForStream to allocate buffers for stream samples.
helpviewer_keywords: ["IWMReaderAdvanced interface [windows Media Format]","SetAllocateForStream method","IWMReaderAdvanced.SetAllocateForStream","IWMReaderAdvanced::SetAllocateForStream","IWMReaderAdvancedSetAllocateForStream","SetAllocateForStream","SetAllocateForStream method [windows Media Format]","SetAllocateForStream method [windows Media Format]","IWMReaderAdvanced interface","wmformat.iwmreaderadvanced_setallocateforstream","wmsdkidl/IWMReaderAdvanced::SetAllocateForStream"]
old-location: wmformat\iwmreaderadvanced_setallocateforstream.htm
tech.root: wmformat
ms.assetid: 58c396a9-5d1e-4a13-a877-5289649a6375
ms.date: 12/05/2018
ms.keywords: IWMReaderAdvanced interface [windows Media Format],SetAllocateForStream method, IWMReaderAdvanced.SetAllocateForStream, IWMReaderAdvanced::SetAllocateForStream, IWMReaderAdvancedSetAllocateForStream, SetAllocateForStream, SetAllocateForStream method [windows Media Format], SetAllocateForStream method [windows Media Format],IWMReaderAdvanced interface, wmformat.iwmreaderadvanced_setallocateforstream, wmsdkidl/IWMReaderAdvanced::SetAllocateForStream
f1_keywords:
- wmsdkidl/IWMReaderAdvanced.SetAllocateForStream
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
- IWMReaderAdvanced.SetAllocateForStream
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderAdvanced::SetAllocateForStream


## -description



The <b>SetAllocateForStream</b> method specifies whether the reader uses <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-allocateforstream">IWMReaderCallbackAdvanced::AllocateForStream</a> to allocate buffers for stream samples.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number. Stream numbers are in the range of 1 through 63.


### -param fAllocate [in]

Boolean value that is True if the reader uses <b>IWMReaderCallbackAdvanced</b> to allocate streams.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



If the application's callback implements the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderallocatorex">IWMReaderAllocatorEx</a> interface interface, the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex">AllocateForStreamEx</a> method is called instead of <b>AllocateForStream</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced">IWMReaderAdvanced Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getallocateforstream">IWMReaderAdvanced::GetAllocateForStream</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex">IWMReaderAllocatorEx::AllocateForStreamEx</a>
 

 

