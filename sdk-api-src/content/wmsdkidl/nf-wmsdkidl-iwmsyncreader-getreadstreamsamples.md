---
UID: NF:wmsdkidl.IWMSyncReader.GetReadStreamSamples
title: IWMSyncReader::GetReadStreamSamples
author: windows-driver-content
description: The GetReadStreamSamples method ascertains whether a stream is configured to deliver compressed samples.
old-location: wmformat\iwmsyncreader_getreadstreamsamples.htm
old-project: wmformat
ms.assetid: cb903723-fd4b-4b1c-aa2f-e3c9f74dcebd
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: GetReadStreamSamples, GetReadStreamSamples method [windows Media Format], GetReadStreamSamples method [windows Media Format],IWMSyncReader interface, IWMSyncReader interface [windows Media Format],GetReadStreamSamples method, IWMSyncReader.GetReadStreamSamples, IWMSyncReader::GetReadStreamSamples, IWMSyncReaderGetReadStreamSamples, wmformat.iwmsyncreader_getreadstreamsamples, wmsdkidl/IWMSyncReader::GetReadStreamSamples
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
-	IWMSyncReader.GetReadStreamSamples
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMSyncReader::GetReadStreamSamples


## -description



The <b>GetReadStreamSamples</b> method ascertains whether a stream is configured to deliver compressed samples.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number.


### -param pfCompressed [out]

Pointer to a flag that receives the status of compressed delivery for the stream specified.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pfCompressed</i> is <b>NULL</b>.

OR

<i>wStreamNum</i> specifies an invalid stream number.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
No file is open in the synchronous reader.

</td>
</tr>
</table>
 




## -remarks



To configure a stream to deliver compressed samples, call <a href="https://msdn.microsoft.com/cf998ecc-e80e-4eb3-9cba-61bd0b665d51">IWMSyncReader::SetReadStreamSamples</a>.




## -see-also




<a href="https://msdn.microsoft.com/2a46e79f-084e-4173-ad0f-211d3065d81a">IWMSyncReader Interface</a>
 

 

