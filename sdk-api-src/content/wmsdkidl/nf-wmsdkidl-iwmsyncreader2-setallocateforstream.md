---
UID: NF:wmsdkidl.IWMSyncReader2.SetAllocateForStream
title: IWMSyncReader2::SetAllocateForStream (wmsdkidl.h)
description: The SetAllocateForStream method sets a sample allocation callback interface for allocating stream samples.
helpviewer_keywords: ["IWMSyncReader2 interface [windows Media Format]","SetAllocateForStream method","IWMSyncReader2.SetAllocateForStream","IWMSyncReader2::SetAllocateForStream","IWMSyncReader2SetAllocateForStream","SetAllocateForStream","SetAllocateForStream method [windows Media Format]","SetAllocateForStream method [windows Media Format]","IWMSyncReader2 interface","wmformat.iwmsyncreader2_setallocateforstream","wmsdkidl/IWMSyncReader2::SetAllocateForStream"]
old-location: wmformat\iwmsyncreader2_setallocateforstream.htm
tech.root: wmformat
ms.assetid: ed94977e-e930-4045-a69d-36109e7e21c9
ms.date: 4/26/2023
ms.keywords: IWMSyncReader2 interface [windows Media Format],SetAllocateForStream method, IWMSyncReader2.SetAllocateForStream, IWMSyncReader2::SetAllocateForStream, IWMSyncReader2SetAllocateForStream, SetAllocateForStream, SetAllocateForStream method [windows Media Format], SetAllocateForStream method [windows Media Format],IWMSyncReader2 interface, wmformat.iwmsyncreader2_setallocateforstream, wmsdkidl/IWMSyncReader2::SetAllocateForStream
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMSyncReader2::SetAllocateForStream
 - wmsdkidl/IWMSyncReader2::SetAllocateForStream
dev_langs:
 - c++
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
---

# IWMSyncReader2::SetAllocateForStream


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetAllocateForStream</b> method sets a sample allocation callback interface for allocating stream samples. This method enables you to use your own buffers for reading samples. Once set, the synchronous reader will call the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex">IWMReaderAllocatorEx::AllocateForStreamEx</a> method every time it needs a buffer to hold a stream sample.

## -parameters

### -param wStreamNum [in]

<b>WORD</b> containing the stream number.

### -param pAllocator [in]

Pointer to an <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderallocatorex">IWMReaderAllocatorEx</a> interface implemented in your application.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/wmformat/allocating-buffers-for-file-reading">Allocating Buffers for File Reading</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader2">IWMSyncReader2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader2-getallocateforstream">IWMSyncReader2::GetAllocateForStream</a>