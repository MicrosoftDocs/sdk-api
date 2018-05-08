---
UID: NF:wmsdkidl.IWMReaderAdvanced.SetStreamsSelected
title: IWMReaderAdvanced::SetStreamsSelected
author: windows-driver-content
description: The SetStreamsSelected method specifies which streams are selected when manual stream selection is enabled.
old-location: wmformat\iwmreaderadvanced_setstreamsselected.htm
old-project: wmformat
ms.assetid: 921ab9fe-757f-4856-9fbc-b615bf92d90f
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: IWMReaderAdvanced interface [windows Media Format],SetStreamsSelected method, IWMReaderAdvanced.SetStreamsSelected, IWMReaderAdvanced::SetStreamsSelected, IWMReaderAdvancedSetStreamsSelected, SetStreamsSelected, SetStreamsSelected method [windows Media Format], SetStreamsSelected method [windows Media Format],IWMReaderAdvanced interface, wmformat.iwmreaderadvanced_setstreamsselected, wmsdkidl/IWMReaderAdvanced::SetStreamsSelected
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmvcore.lib
-	Wmvcore.dll
-	WMStubDRM.lib
-	WMStubDRM.dll
api_name:
-	IWMReaderAdvanced.SetStreamsSelected
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderAdvanced::SetStreamsSelected


## -description



The <b>SetStreamsSelected</b> method specifies which streams are selected when manual stream selection is enabled.




## -parameters




### -param cStreamCount [in]

<b>WORD</b> containing the count of stream numbers in the <i>pwStreamNumbers</i> array.


### -param pwStreamNumbers [in]

Pointer to an array containing the stream numbers. Stream numbers are in the range of 1 through 63.


### -param pSelections [in]

Pointer to an array, of equal length to <i>pwStreamNumbers</i>, with each entry containing one member of the <a href="https://msdn.microsoft.com/7191d608-1a25-48c0-858b-c5e93f9d8e6e">WMT_STREAM_SELECTION</a> enumeration type.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for an unspecified reason.

</td>
</tr>
</table>
 




## -remarks



This method enables the selected state of multiple streams to be changed simultaneously. Multiple streams can then be turned on or off at the exact time required. For this reason, the parameters of this method and the <b>GetStreamSelected</b> method are not identical.

When selecting streams manually, you should select only one stream at a time from each set of mutually exclusive streams in a file. The SDK does not prevent you from selecting multiple mutually exclusive streams, but the samples for all mutually exclusive streams will be delivered to <a href="https://msdn.microsoft.com/0f6e4d4f-4295-44ff-95bc-e683bdbab8e0">IWMReaderCallback::OnSample</a> using the same output number. This makes it difficult to differentiate between samples from the various streams.

To deliver samples by stream number, you must receive uncompressed stream samples. You can receive stream samples for a specific stream by calling <a href="https://msdn.microsoft.com/3fb39726-7f43-41ec-9ead-38456b5cd964">IWMReaderAdvanced::SetReceiveStreamSamples</a>. You must also implement <b>IWMReaderCallbackAdvanced::OnStreamSample</b>.




## -see-also




<a href="https://msdn.microsoft.com/a7a20f87-6f21-4fe8-8889-1b6689daf833">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/083fc743-79be-43c6-ac4b-458c74f42fa0">IWMReaderAdvanced::GetStreamSelected</a>



<a href="https://msdn.microsoft.com/49ec283f-670a-4a0e-9477-c60a80919a1e">To Use Manual Stream Selection</a>
 

 

