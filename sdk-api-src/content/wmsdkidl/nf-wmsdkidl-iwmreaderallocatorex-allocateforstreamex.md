---
UID: NF:wmsdkidl.IWMReaderAllocatorEx.AllocateForStreamEx
title: IWMReaderAllocatorEx::AllocateForStreamEx (wmsdkidl.h)
description: The AllocateForStreamEx method allocates a user-created buffer for samples delivered to the IWMReaderCallbackAdvanced::OnStreamSample method.
helpviewer_keywords: ["AllocateForStreamEx","AllocateForStreamEx method [windows Media Format]","AllocateForStreamEx method [windows Media Format]","IWMReaderAllocatorEx interface","IWMReaderAllocatorEx interface [windows Media Format]","AllocateForStreamEx method","IWMReaderAllocatorEx.AllocateForStreamEx","IWMReaderAllocatorEx::AllocateForStreamEx","IWMReaderAllocatorExAllocateForStreamEx","wmformat.iwmreaderallocatorex_allocateforstreamex","wmsdkidl/IWMReaderAllocatorEx::AllocateForStreamEx"]
old-location: wmformat\iwmreaderallocatorex_allocateforstreamex.htm
tech.root: wmformat
ms.assetid: bb12f0e1-dc9c-447e-a28d-30c45eb95d09
ms.date: 4/26/2023
ms.keywords: AllocateForStreamEx, AllocateForStreamEx method [windows Media Format], AllocateForStreamEx method [windows Media Format],IWMReaderAllocatorEx interface, IWMReaderAllocatorEx interface [windows Media Format],AllocateForStreamEx method, IWMReaderAllocatorEx.AllocateForStreamEx, IWMReaderAllocatorEx::AllocateForStreamEx, IWMReaderAllocatorExAllocateForStreamEx, wmformat.iwmreaderallocatorex_allocateforstreamex, wmsdkidl/IWMReaderAllocatorEx::AllocateForStreamEx
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMReaderAllocatorEx::AllocateForStreamEx
 - wmsdkidl/IWMReaderAllocatorEx::AllocateForStreamEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmsdkidl.h
api_name:
 - IWMReaderAllocatorEx.AllocateForStreamEx
---

# IWMReaderAllocatorEx::AllocateForStreamEx


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AllocateForStreamEx</b> method allocates a user-created buffer for samples delivered to the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample">IWMReaderCallbackAdvanced::OnStreamSample</a> method.

## -parameters

### -param wStreamNum [in]

<b>WORD</b> containing the stream number.

### -param cbBuffer [in]

Size of <i>ppBuffer</i>, in bytes.

### -param ppBuffer [out]

Pointer to a pointer to an <b>INSSBuffer</b> object.

### -param dwFlags [in]

<b>DWORD</b> containing the relevant flags.

<table>
<tr>
<th>Flag
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WM_SFEX_NOTASYNCPOINT</td>
<td>This flag is the opposite of the WM_SF_CLEANPOINT flag used in other methods of this SDK. It indicates that the point is not a <a href="/windows/desktop/wmformat/wmformat-glossary">key frame</a>, or is not a good point to go to during a seek. This inverse definition is used for compatibility with Direct Show.</td>
</tr>
<tr>
<td>WM_SFEX_DATALOSS</td>
<td>Some data has been lost between the previous sample and the sample with the flag set.</td>
</tr>
</table>

### -param cnsSampleTime [in]

Specifies the sample time, in 100-nanosecond units.

### -param cnsSampleDuration [in]

Specifies the sample duration, in 100-nanosecond units.

### -param pvContext [in]

Generic pointer, for use by the application. This pointer is the context pointer given to the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-start">IWMReader::Start</a> method.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

This method differs from <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-allocateforstream">IWMReaderCallbackAdvanced::AllocateForStream</a> in that sample time and duration values can be passed.

When you allocate a sample in your implementation of this method, you should call <a href="/previous-versions/windows/desktop/api/wmsbuffer/nf-wmsbuffer-inssbuffer-setlength">INSSBuffer::SetLength</a> to set the length of the buffer to the length passed by the reader in the <i>cbBuffer</i> parameter. If you do not set the current length on the buffer, the reader may encounter an error.

## -see-also

<a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderallocatorex">IWMReaderAllocatorEx Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced">IWMReaderCallbackAdvanced Interface</a>