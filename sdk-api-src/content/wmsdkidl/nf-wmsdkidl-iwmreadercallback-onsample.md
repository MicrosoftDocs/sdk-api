---
UID: NF:wmsdkidl.IWMReaderCallback.OnSample
title: IWMReaderCallback::OnSample (wmsdkidl.h)
description: The OnSample method is called during the reading of a file (due to a Start call) indicating that new data is available.helpviewer_keywords: ["IWMReaderCallback interface [windows Media Format]","OnSample method","IWMReaderCallback.OnSample","IWMReaderCallback::OnSample","IWMReaderCallbackOnSample","OnSample","OnSample method [windows Media Format]","OnSample method [windows Media Format]","IWMReaderCallback interface","wmformat.iwmreadercallback_onsample","wmsdkidl/IWMReaderCallback::OnSample"]
old-location: wmformat\iwmreadercallback_onsample.htm
tech.root: wmformat
ms.assetid: 0f6e4d4f-4295-44ff-95bc-e683bdbab8e0
ms.date: 12/05/2018
ms.keywords: IWMReaderCallback interface [windows Media Format],OnSample method, IWMReaderCallback.OnSample, IWMReaderCallback::OnSample, IWMReaderCallbackOnSample, OnSample, OnSample method [windows Media Format], OnSample method [windows Media Format],IWMReaderCallback interface, wmformat.iwmreadercallback_onsample, wmsdkidl/IWMReaderCallback::OnSample
f1_keywords:
- wmsdkidl/IWMReaderCallback.OnSample
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
- IWMReaderCallback.OnSample
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderCallback::OnSample


## -description



The <b>OnSample</b> method is called during the reading of a file (due to a <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-start">Start</a> call) indicating that new data is available.




## -parameters




### -param dwOutputNum [in]

<b>DWORD</b> containing the number of the output to which the sample belongs.


### -param cnsSampleTime [in]

<b>QWORD</b> containing the sample time, in 100-nanosecond units.


### -param cnsSampleDuration [in]

<b>QWORD</b> containing the sample duration, in 100-nanosecond units. For video streams, if the SampleDuration data unit extension was set on this sample when the file was created, then this parameter will contain that value. For more information on SampleDuration , see <a href="https://docs.microsoft.com/windows/desktop/api/wmsbuffer/nf-wmsbuffer-inssbuffer3-getproperty">INSSBuffer3::GetProperty</a>.


### -param dwFlags [in]

The flags that can be specified in <i>dwFlags</i> have the following uses.

<table>
<tr>
<th>Flag
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>No flag set</td>
<td>None of the conditions for the other flags applies. For example, a <a href="https://docs.microsoft.com/windows/desktop/wmformat/wmformat-glossary">delta frame</a> in most cases would not have any flags set for it.</td>
</tr>
<tr>
<td>WM_SF_CLEANPOINT</td>
<td>This is the same as a <a href="https://docs.microsoft.com/windows/desktop/wmformat/wmformat-glossary">key frame</a>. It indicates a good point to go to during a seek, for example.</td>
</tr>
<tr>
<td>WM_SF_DISCONTINUITY</td>
<td>The data stream has a gap in it, which could be due to a seek, a network loss, or other reason. This can be useful extra information for an application such as a codec or renderer. The flag is set on the first piece of data following the gap.</td>
</tr>
<tr>
<td>WM_SF_DATALOSS</td>
<td>Some data has been lost between the previous sample and the sample with this flag set.</td>
</tr>
</table>
 


### -param pSample [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer</a> interface of an object containing the sample. The reader calls <b>SAFE_RELEASE</b> on this pointer after your <b>OnSample</b> method returns. You can call <b>AddRef</b> on this pointer if you need to keep a reference count on the buffer. Do not call <b>Release</b> on this pointer unless you have called <b>AddRef</b>.


### -param pvContext [in]

Generic pointer, for use by the application. This pointer is the context pointer given to the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-start">IWMReader::Start</a> method.


## -returns



To use this method, you must implement it in your application. The method should always return S_OK.




## -remarks



This method is for receipt of uncompressed samples by output number only. If you need to receive samples for multiple streams in a single output (as in the case of mutually exclusive streams), you must use <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample">IWMReaderCallbackAdvanced::OnStreamSample</a>. In this case, you will receive compressed samples. There is no way to use the reader to receive uncompressed samples by stream number.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback">IWMReaderCallback Interface</a>
 

 

