---
UID: NF:spatialaudioclient.ISpatialAudioClient.IsSpatialAudioStreamAvailable
title: ISpatialAudioClient::IsSpatialAudioStreamAvailable
author: windows-sdk-content
description: When successful, gets a value indicating whether the currently active spatial rendering engine supports the specified spatial audio render stream.
old-location: coreaudio\ispatialaudioclient_isspatialaudiostreamavailable.htm
old-project: CoreAudio
ms.assetid: 4CE8A0D2-8B0B-4628-99DE-5B588842D7C5
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: ISpatialAudioClient interface [Core Audio],IsSpatialAudioStreamAvailable method, ISpatialAudioClient.IsSpatialAudioStreamAvailable, ISpatialAudioClient::IsSpatialAudioStreamAvailable, IsSpatialAudioStreamAvailable, IsSpatialAudioStreamAvailable method [Core Audio], IsSpatialAudioStreamAvailable method [Core Audio],ISpatialAudioClient interface, coreaudio.ispatialaudioclient_isspatialaudiostreamavailable, spatialaudioclient/ISpatialAudioClient::IsSpatialAudioStreamAvailable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: spatialaudioclient.h
req.include-header: 
req.redist: 
req.target-type: Windows
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
tech.root: 
req.typenames: AudioObjectType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - spatialaudioclient.h
api_name:
 - ISpatialAudioClient.IsSpatialAudioStreamAvailable
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISpatialAudioClient::IsSpatialAudioStreamAvailable


## -description


When successful, gets a value indicating whether the currently active spatial rendering engine supports the specified spatial audio render stream. 


## -parameters




### -param streamUuid [in]

The interface ID of the interface for which availability is queried.


### -param auxiliaryInfo [in, optional]

A structure containing additional information to be used when support is queried. For more information, see Remarks.


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUDCLNT_E_STREAM_IS_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The specified stream interface can't be activated by the currently active rendering engine.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUDCLNT_E_METADATA_FORMAT_IS_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The metadata format supplied in the <i>auxiliaryInfo</i> parameter is not supported by the current rendering engine. For more information, see Remarks..

</td>
</tr>
</table>
 




## -remarks



When querying to see if the <a href="https://msdn.microsoft.com/1623B280-FC12-4C19-9D4A-D8463D1A1046">ISpatialAudioObjectRenderStreamForMetadata</a> you can use the auxilaryInfo parameter to query if a particular metadata format is supported. The following code example demonstrates how to initialize the <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure to check for support for an example metadata format.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>PROPVARIANT auxiliaryInfo;  
auxiliaryInfo.vt = VT_CLSID;  
auxiliaryInfo.puuid = const_cast&lt;CLSID*&gt;(&amp;CONTOSO_SPATIAL_METADATA_V1_0);  </pre>
</td>
</tr>
</table></span></div>
If the specified metadata format is unsupported, <b>IsSpatialAudioStreamAvailable</b> returns SPTLAUDCLNT_E_METADATA_FORMAT_IS_NOT_SUPPORTED.




## -see-also




<a href="https://msdn.microsoft.com/950778D4-79FE-4222-951F-5A456A633124">ISpatialAudioClient</a>
 

 

