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

# IMFASFIndexer::GetSeekPositionForValue


## -description



          Given a desired seek time, gets the offset from which the client should start reading data.
        


## -parameters




### -param pvarValue [in]


            The value of the index entry for which to get the position. The format of this value varies depending on the type of index, which is specified in the index identifier. For time-based indexing, the variant type is <b>VT_I8</b> and the value is the desired seek time, in 100-nanosecond units.
          


### -param pIndexIdentifier [in]


            Pointer to an <a href="https://msdn.microsoft.com/8103a62e-6d1a-4dcd-af91-cedb30523004">ASF_INDEX_IDENTIFIER</a> structure that identifies the stream number and index type.
          


### -param pcbOffsetWithinData [out]


            Receives the offset within the data segment of the ASF Data Object. The offset is in bytes, and is relative to the start of packet 0. The offset gives the starting location from which the client should begin reading from the stream. This location might not correspond exactly to the requested seek time.
          


            For reverse playback, if no key frame exists after the desired seek position, this parameter receives the value <b>MFASFINDEXER_READ_FOR_REVERSEPLAYBACK_OUTOFDATASEGMENT</b>. In that case, the seek position should be 1 byte pass the end of the data segment.
          


### -param phnsApproxTime [out]


            Receives the approximate time stamp of the data that is located at the offset returned in the <i>pcbOffsetWithinData</i> parameter. The accuracy of this value is equal to the indexing interval of the ASF index, typically about 1 second.
          

<ul>
<li>
                If the index type specified in <i>pIndexIdentifier</i> is <b>GUID_NULL</b> (time indexing), this parameter can be <b>NULL</b>.
              </li>
<li>
                For all other index types, this parameter must be <b>NULL</b>.
              </li>
</ul>

            If the approximate time stamp cannot be determined, this parameter receives the value <b>MFASFINDEXER_APPROX_SEEK_TIME_UNKNOWN</b>.
          


### -param pdwPayloadNumberOfStreamWithinPacket [out]


            Receives the payload number of the payload that contains the information for the specified stream. Packets can contain multiple payloads, each containing data for a different stream. This parameter can be <b>NULL</b>.
          


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
<dt><b>MF_E_ASF_OUTOFRANGE</b></dt>
</dl>
</td>
<td width="60%">

                The requested seek time is out of range.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NO_INDEX</b></dt>
</dl>
</td>
<td width="60%">

                No index exists of the specified type for the specified stream.
              

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3f95b0ac-d70f-4bc2-8524-c7de1df34afa">ASF Index Object</a>



<a href="https://msdn.microsoft.com/93127fe4-bca9-4674-ae21-012367d7dd2f">IMFASFIndexer</a>



<a href="https://msdn.microsoft.com/9273ff1f-382e-4c58-b571-4852545915b3">MFTIME</a>
 

 

