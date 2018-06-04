---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWMSyncReader::SetStreamsSelected


## -description



The <b>SetStreamsSelected</b> method configures the samples to be delivered from a list of streams. Each stream can be set to deliver all samples, no samples, or only <a href="wmformat_glossary.htm">cleanpoint</a> samples.




## -parameters




### -param cStreamCount [in]

Count of streams listed at <i>pwStreamNumbers</i>.


### -param pwStreamNumbers [in]

Pointer to an array of <b>WORD</b> values containing the stream numbers.


### -param pSelections [in]

Pointer to an array of <a href="https://msdn.microsoft.com/7191d608-1a25-48c0-858b-c5e93f9d8e6e">WMT_STREAM_SELECTION</a> enumeration values. These values correspond with the stream numbers listed at <i>pwStreamNumbers</i>. Each value specifies the samples to deliver for the appropriate stream.


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
<i>pwStreamNumbers</i> or <i>pSelections</i> is <b>NULL</b>.

OR

<i>cStreamCount</i> is zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
No file is loaded in the synchronous reader.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method is unable to allocate memory for an internal object.

</td>
</tr>
</table>
 




## -remarks



You can call <b>SetStreamsSelects</b> at any time after a file has been loaded into the synchronous reader. You can continue making calls as needed during playback.

This method is identical to <a href="https://msdn.microsoft.com/921ab9fe-757f-4856-9fbc-b615bf92d90f">IWMReaderAdvanced::SetStreamsSelected</a> except that, in the synchronous reader, stream selection is always manual. Also, because <a href="https://msdn.microsoft.com/948047b3-3b87-4381-9320-c9602716ade2">IWMSyncReader::GetNextSample</a> includes a stream number output, you can select as many mutually exclusive streams as you like and receive samples for them.




## -see-also




<a href="https://msdn.microsoft.com/2a46e79f-084e-4173-ad0f-211d3065d81a">IWMSyncReader Interface</a>
 

 

