---
UID: NF:wmsdkidl.IWMReaderCallbackAdvanced.AllocateForOutput
title: IWMReaderCallbackAdvanced::AllocateForOutput (wmsdkidl.h)
description: The AllocateForOutput method allocates user-created buffers for samples delivered to IWMReaderCallback::OnSample. For more information about allocating your own buffers, see User Allocated Sample Support.helpviewer_keywords: ["AllocateForOutput","AllocateForOutput method [windows Media Format]","AllocateForOutput method [windows Media Format]","IWMReaderCallbackAdvanced interface","IWMReaderCallbackAdvanced interface [windows Media Format]","AllocateForOutput method","IWMReaderCallbackAdvanced.AllocateForOutput","IWMReaderCallbackAdvanced::AllocateForOutput","IWMReaderCallbackAdvancedAllocateForOutput","wmformat.iwmreadercallbackadvanced_allocateforoutput","wmsdkidl/IWMReaderCallbackAdvanced::AllocateForOutput"]
old-location: wmformat\iwmreadercallbackadvanced_allocateforoutput.htm
tech.root: wmformat
ms.assetid: bd7340c9-9380-4dba-b8ac-2a616ce9949f
ms.date: 12/05/2018
ms.keywords: AllocateForOutput, AllocateForOutput method [windows Media Format], AllocateForOutput method [windows Media Format],IWMReaderCallbackAdvanced interface, IWMReaderCallbackAdvanced interface [windows Media Format],AllocateForOutput method, IWMReaderCallbackAdvanced.AllocateForOutput, IWMReaderCallbackAdvanced::AllocateForOutput, IWMReaderCallbackAdvancedAllocateForOutput, wmformat.iwmreadercallbackadvanced_allocateforoutput, wmsdkidl/IWMReaderCallbackAdvanced::AllocateForOutput
f1_keywords:
- wmsdkidl/IWMReaderCallbackAdvanced.AllocateForOutput
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wmsdkidl.h
api_name:
- IWMReaderCallbackAdvanced.AllocateForOutput
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderCallbackAdvanced::AllocateForOutput


## -description



The <b>AllocateForOutput</b> method allocates user-created buffers for samples delivered to <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample">IWMReaderCallback::OnSample</a>. For more information about allocating your own buffers, see <a href="https://docs.microsoft.com/windows/desktop/wmformat/user-allocated-sample-support">User Allocated Sample Support</a>.




## -parameters




### -param dwOutputNum [in]

<b>DWORD</b> containing the output number.


### -param cbBuffer [in]

Size of the buffer, in bytes.


### -param ppBuffer [out]

If the method succeeds, returns a pointer to a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer</a> interface.


### -param pvContext [in]

Generic pointer, for use by the application. This pointer is the context pointer given to the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-start">IWMReader::Start</a> method.


## -returns



To use this method, you must implement it in your application. You can return whatever <b>HRESULT</b> error codes are appropriate to your implementation. For more information about the <b>HRESULT</b> error codes included for use by the Windows Media Format SDK, see <a href="https://docs.microsoft.com/windows/desktop/wmformat/error-codes">Error Codes</a>.




## -remarks



An extended version of this method called <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex">AllocateForOutputEx</a> exists in the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderallocatorex">IWMReaderAllocatorEx</a> interface.

When allocating buffers, you can use whatever logic suits your application. Typically, applications initialize a pool of buffers for the file or a pool of buffers for each stream or output. When the application is done with a sample, the buffer is put back into the pool for use.

You can determine the size needed to hold the largest sample of an output by calling <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxoutputsamplesize">IWMReaderAdvanced::GetMaxOutputSampleSize</a>. This is the size you should make the samples in the pool used for the output.

When you allocate a sample in your implementation of this method, you should call <a href="https://docs.microsoft.com/windows/desktop/api/wmsbuffer/nf-wmsbuffer-inssbuffer-setlength">INSSBuffer::SetLength</a> to set the length of the buffer to the length passed by the reader in the <i>cbBuffer</i> parameter. If you do not set the current length on the buffer, the reader may encounter an error.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced">IWMReaderCallbackAdvanced Interface</a>
 

 

