---
UID: NF:wmsdkidl.IWMSyncReader.SetReadStreamSamples
title: IWMSyncReader::SetReadStreamSamples
author: windows-sdk-content
description: The SetReadStreamSamples method specifies whether samples from a stream will be delivered compressed or uncompressed.
old-location: wmformat\iwmsyncreader_setreadstreamsamples.htm
tech.root: wmformat
ms.assetid: cf998ecc-e80e-4eb3-9cba-61bd0b665d51
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IWMSyncReader interface [windows Media Format],SetReadStreamSamples method, IWMSyncReader.SetReadStreamSamples, IWMSyncReader::SetReadStreamSamples, IWMSyncReaderSetReadStreamSamples, SetReadStreamSamples, SetReadStreamSamples method [windows Media Format], SetReadStreamSamples method [windows Media Format],IWMSyncReader interface, wmformat.iwmsyncreader_setreadstreamsamples, wmsdkidl/IWMSyncReader::SetReadStreamSamples
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
 - IWMSyncReader.SetReadStreamSamples
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMSyncReader::SetReadStreamSamples


## -description



The <b>SetReadStreamSamples</b> method specifies whether samples from a stream will be delivered compressed or uncompressed.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number.


### -param fCompressed [in]

Boolean value that is True if samples will be compressed.


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
No file is open in the synchronous reader.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_PROTECTED_CONTENT</b></dt>
</dl>
</td>
<td width="60%">
The stream is protected and not configured to deliver compressed samples.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>wStreamNum</i> specifies an invalid stream number.

</td>
</tr>
</table>
 




## -remarks



You can call <b>SetReadStreamSamples</b> at any time after a file has been loaded into the synchronous reader. You can continue making calls as needed during playback.




## -see-also




<a href="https://msdn.microsoft.com/2a46e79f-084e-4173-ad0f-211d3065d81a">IWMSyncReader Interface</a>



<a href="https://msdn.microsoft.com/cb903723-fd4b-4b1c-aa2f-e3c9f74dcebd">IWMSyncReader::GetReadStreamSamples</a>
 

 

