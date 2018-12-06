---
UID: NF:wmsdkidl.IWMReaderCallbackAdvanced.OnStreamSample
title: IWMReaderCallbackAdvanced::OnStreamSample
author: windows-sdk-content
description: The OnStreamSample method delivers stream samples from the source file without decompressing them first.
old-location: wmformat\iwmreadercallbackadvanced_onstreamsample.htm
tech.root: wmformat
ms.assetid: 6bfdd903-a3a4-4ef4-b88a-4d24c9c0f4b8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMReaderCallbackAdvanced interface [windows Media Format],OnStreamSample method, IWMReaderCallbackAdvanced.OnStreamSample, IWMReaderCallbackAdvanced::OnStreamSample, IWMReaderCallbackAdvancedOnStreamSample, OnStreamSample, OnStreamSample method [windows Media Format], OnStreamSample method [windows Media Format],IWMReaderCallbackAdvanced interface, wmformat.iwmreadercallbackadvanced_onstreamsample, wmsdkidl/IWMReaderCallbackAdvanced::OnStreamSample
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWMReaderCallbackAdvanced.OnStreamSample
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderCallbackAdvanced::OnStreamSample


## -description



The <b>OnStreamSample</b> method delivers stream samples from the source file without decompressing them first.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number.


### -param cnsSampleTime [in]

<b>QWORD</b> containing the sample time, in 100-nanosecond units.


### -param cnsSampleDuration [in]

<b>QWORD</b> containing the sample duration, in 100-nanosecond units.


### -param dwFlags [in]

The flags that can be specified have the following uses.

<table>
<tr>
<th>Flag
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>No flag set</td>
<td>None of the conditions for the other flags applies. For example, a <a href="wmformat_glossary.htm">delta frame</a> in most cases would not have any flags set for it.</td>
</tr>
<tr>
<td>WM_SF_CLEANPOINT</td>
<td>This is the same as a <a href="wmformat_glossary.htm">key frame</a>. It indicates a good point to go to during a seek, for example.</td>
</tr>
<tr>
<td>WM_SF_DISCONTINUITY</td>
<td>The data stream has a gap in it, which could be due to a seek, a network loss, or other reason. This can be useful extra information for an application such as a codec or renderer. The flag is set on the first piece of data following the gap.</td>
</tr>
<tr>
<td>WM_SF_DATALOSS</td>
<td>Some data has been lost between the previous sample, and the sample with this flag set.</td>
</tr>
</table>
 


### -param pSample [in]

Pointer to a sample stored in an <a href="https://msdn.microsoft.com/c47c016a-e7eb-4a2c-b365-5537749db5bc">INSSBuffer</a> interface. The reader calls <b>SAFE_RELEASE</b> on this pointer after your <b>OnStreamSample</b> method returns. You can call <b>AddRef</b> on this pointer if you need to keep a reference count on the buffer. Do not call <b>Release</b> on this pointer unless you have called <b>AddRef</b>.


### -param pvContext [in]

Generic pointer, for use by the application.


## -returns



To use this method, you must implement it in your application. You can return whatever <b>HRESULT</b> error codes are appropriate to your implementation. For more information about the <b>HRESULT</b> error codes included for use by the Windows Media Format SDK, see <a href="https://msdn.microsoft.com/ea1c129b-c0d7-4a1b-934c-c1c07364d4a8">Error Codes</a>.




## -remarks



When using the asynchronous reader, only compressed samples can be delivered for a stream number. If you want to retrieve uncompressed samples by stream number, you should use the synchronous reader.

There are many reasons why you might want to retrieve compressed samples. The most common use is to transfer a stream from one ASF file to another.

If you receive compressed samples, you must either keep them compressed, or decompress them with your application. The Windows Media Format SDK does not provide methods to decompress samples once they have been removed from a file.

This method is not able to deliver secure content. If protected content is used, the method will return NS_E_PROTECTEDCONTENT.

The samples delivered by this method are compressed, but are in all other ways exactly the same as samples delivered through <a href="https://msdn.microsoft.com/0f6e4d4f-4295-44ff-95bc-e683bdbab8e0">IWMReaderCallback::OnSample</a>.

To get samples for a particular stream, call <a href="https://msdn.microsoft.com/3fb39726-7f43-41ec-9ead-38456b5cd964">IWMReaderAdvanced::SetReceiveStreamSamples</a>.




## -see-also




<a href="https://msdn.microsoft.com/9d18961a-5ea4-4f3e-b473-7399e155f800">IWMReaderCallbackAdvanced Interface</a>
 

 

