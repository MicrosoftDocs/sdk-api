---
UID: NF:wmsdkidl.IWMWriterPostViewCallback.OnPostViewSample
title: IWMWriterPostViewCallback::OnPostViewSample (wmsdkidl.h)
description: The OnPostViewSample method is called when new postview data is available. The application implements this method.helpviewer_keywords: ["IWMWriterPostViewCallback interface [windows Media Format]","OnPostViewSample method","IWMWriterPostViewCallback.OnPostViewSample","IWMWriterPostViewCallback::OnPostViewSample","IWMWriterPostViewCallbackOnPostViewSample","OnPostViewSample","OnPostViewSample method [windows Media Format]","OnPostViewSample method [windows Media Format]","IWMWriterPostViewCallback interface","wmformat.iwmwriterpostviewcallback_onpostviewsample","wmsdkidl/IWMWriterPostViewCallback::OnPostViewSample"]
old-location: wmformat\iwmwriterpostviewcallback_onpostviewsample.htm
tech.root: wmformat
ms.assetid: 5d29a746-70fe-495e-a7f2-dbf085829496
ms.date: 12/05/2018
ms.keywords: IWMWriterPostViewCallback interface [windows Media Format],OnPostViewSample method, IWMWriterPostViewCallback.OnPostViewSample, IWMWriterPostViewCallback::OnPostViewSample, IWMWriterPostViewCallbackOnPostViewSample, OnPostViewSample, OnPostViewSample method [windows Media Format], OnPostViewSample method [windows Media Format],IWMWriterPostViewCallback interface, wmformat.iwmwriterpostviewcallback_onpostviewsample, wmsdkidl/IWMWriterPostViewCallback::OnPostViewSample
f1_keywords:
- wmsdkidl/IWMWriterPostViewCallback.OnPostViewSample
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
- IWMWriterPostViewCallback.OnPostViewSample
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMWriterPostViewCallback::OnPostViewSample


## -description



The <b>OnPostViewSample</b> method is called when new postview data is available. The application implements this method.




## -parameters




### -param wStreamNumber [in]

<b>WORD</b> containing the stream number.


### -param cnsSampleTime [in]

Sample time, in 100-nanosecond units.


### -param cnsSampleDuration [in]

Sample duration, in 100-nanosecond units. This will usually be 10000 (1 millisecond).


### -param dwFlags [in]

<b>DWORD</b> containing none, one, or more of the following flags.

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
<td>This is basically the same as a key frame. It indicates a good point to go to during a seek, for example.</td>
</tr>
<tr>
<td>WM_SF_DISCONTINUITY</td>
<td>The data stream has a gap in it, which could be due to a seek, a network loss, or some other reason. This can be useful extra information for an application such as a codec or renderer. The flag is set on the first piece of data following the gap.</td>
</tr>
<tr>
<td>WM_SF_DATALOSS</td>
<td>Some data has been lost between the previous sample and the sample with this flag set.</td>
</tr>
</table>
 


### -param pSample [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer</a> interface on an object that contains the sample.


### -param pvContext [in]

Generic pointer, for use by the application.


## -returns



This method is implemented by the application. It should return S_OK.




## -remarks



Postview data is available only for video.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample">IWMReaderCallback::OnSample</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback">IWMWriterPostViewCallback Interface</a>
 

 

