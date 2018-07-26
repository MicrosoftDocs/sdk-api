---
UID: NF:wmsdkidl.IWMWriterPostViewCallback.OnPostViewSample
title: IWMWriterPostViewCallback::OnPostViewSample
author: windows-sdk-content
description: The OnPostViewSample method is called when new postview data is available. The application implements this method.
old-location: wmformat\iwmwriterpostviewcallback_onpostviewsample.htm
old-project: wmformat
ms.assetid: 5d29a746-70fe-495e-a7f2-dbf085829496
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IWMWriterPostViewCallback interface [windows Media Format],OnPostViewSample method, IWMWriterPostViewCallback.OnPostViewSample, IWMWriterPostViewCallback::OnPostViewSample, IWMWriterPostViewCallbackOnPostViewSample, OnPostViewSample, OnPostViewSample method [windows Media Format], OnPostViewSample method [windows Media Format],IWMWriterPostViewCallback interface, wmformat.iwmwriterpostviewcallback_onpostviewsample, wmsdkidl/IWMWriterPostViewCallback::OnPostViewSample
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WM_AETYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmsdkidl.h
api_name:
 - IWMWriterPostViewCallback.OnPostViewSample
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
<th>
                  Flag
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>No flag set</td>
<td>None of the conditions for the other flags applies. For example, a <a href="https://msdn.microsoft.com/library/Dd757828(v=VS.85).aspx">delta frame</a> in most cases would not have any flags set for it.</td>
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

Pointer to an <a href="https://msdn.microsoft.com/c47c016a-e7eb-4a2c-b365-5537749db5bc">INSSBuffer</a> interface on an object that contains the sample.


### -param pvContext [in]

Generic pointer, for use by the application.


## -returns



This method is implemented by the application. It should return S_OK.




## -remarks



Postview data is available only for video.




## -see-also




<a href="https://msdn.microsoft.com/0f6e4d4f-4295-44ff-95bc-e683bdbab8e0">IWMReaderCallback::OnSample</a>



<a href="https://msdn.microsoft.com/987dd3b4-2245-4640-820c-5a9660ab5e37">IWMWriterPostViewCallback Interface</a>
 

 

