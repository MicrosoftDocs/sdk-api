---
UID: NF:wmsdkidl.IWMSyncReader2.SetAllocateForStream
title: IWMSyncReader2::SetAllocateForStream (wmsdkidl.h)
description: The SetAllocateForStream method sets a sample allocation callback interface for allocating stream samples.helpviewer_keywords: ["IWMSyncReader2 interface [windows Media Format]","SetAllocateForStream method","IWMSyncReader2.SetAllocateForStream","IWMSyncReader2::SetAllocateForStream","IWMSyncReader2SetAllocateForStream","SetAllocateForStream","SetAllocateForStream method [windows Media Format]","SetAllocateForStream method [windows Media Format]","IWMSyncReader2 interface","wmformat.iwmsyncreader2_setallocateforstream","wmsdkidl/IWMSyncReader2::SetAllocateForStream"]
old-location: wmformat\iwmsyncreader2_setallocateforstream.htm
tech.root: wmformat
ms.assetid: ed94977e-e930-4045-a69d-36109e7e21c9
ms.date: 12/05/2018
ms.keywords: IWMSyncReader2 interface [windows Media Format],SetAllocateForStream method, IWMSyncReader2.SetAllocateForStream, IWMSyncReader2::SetAllocateForStream, IWMSyncReader2SetAllocateForStream, SetAllocateForStream, SetAllocateForStream method [windows Media Format], SetAllocateForStream method [windows Media Format],IWMSyncReader2 interface, wmformat.iwmsyncreader2_setallocateforstream, wmsdkidl/IWMSyncReader2::SetAllocateForStream
f1_keywords:
- wmsdkidl/IWMSyncReader2.SetAllocateForStream
dev_langs:
- c++
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
- IWMSyncReader2.SetAllocateForStream
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMSyncReader2::SetAllocateForStream


## -description



The <b>SetAllocateForStream</b> method sets a sample allocation callback interface for allocating stream samples. This method enables you to use your own buffers for reading samples. Once set, the synchronous reader will call the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex">IWMReaderAllocatorEx::AllocateForStreamEx</a> method every time it needs a buffer to hold a stream sample.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number.


### -param pAllocator [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderallocatorex">IWMReaderAllocatorEx</a> interface implemented in your application.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/allocating-buffers-for-file-reading">Allocating Buffers for File Reading</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader2">IWMSyncReader2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader2-getallocateforstream">IWMSyncReader2::GetAllocateForStream</a>
 

 

