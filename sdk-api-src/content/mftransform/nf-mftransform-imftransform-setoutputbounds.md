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

# IMFTransform::SetOutputBounds


## -description



          Sets the range of time stamps the client needs for output.
        


## -parameters




### -param hnsLowerBound


            Specifies the earliest time stamp. The Media Foundation transform (MFT) will accept input until it can produce an output sample that begins at this time; or until it can produce a sample that ends at this time or later. If there is no lower bound, use the value <b>MFT_OUTPUT_BOUND_LOWER_UNBOUNDED</b>.
          


### -param hnsUpperBound


            Specifies the latest time stamp. The MFT will not produce an output sample with time stamps later than this time. If there is no upper bound, use the value <b>MFT_OUTPUT_BOUND_UPPER_UNBOUNDED</b>.
          


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">

                Not implemented.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_TRANSFORM_TYPE_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">

                The media type is not set on one or more streams.
              

</td>
</tr>
</table>
 




## -remarks




        This method can be used to optimize preroll, especially in formats that have gaps between time stamps, or formats where the data must start on a sync point, such as MPEG-2. Calling this method is optional, and implementation of this method by an MFT is optional. If the MFT does not implement the method, the return value is <b>E_NOTIMPL</b>.


        If an MFT implements this method, it must limit its output data to the range of times specified by <i>hnsLowerBound</i> and <i>hnsUpperBound</i>. The MFT discards any input data that is not needed to produce output within this range. If the sample boundaries do not exactly match the range, the MFT should split the output samples, if possible. Otherwise, the output samples can overlap the range.
      


        For example, suppose the output range is 100 to 150 milliseconds (ms), and the output format is video with each frame lasting 33 ms. A sample with a time stamp of 67 ms overlaps the range (67 + 33 = 100) and is produced as output. A sample with a time stamp of  66 ms is discarded (66 + 33 = 99). Similarly, a sample with a time stamp of 150 ms is produced as output, but a sample with a time stamp of 151 is discarded.

If <b>MFT_UNIQUE_METHOD_NAMES</b> is defined before including mftransform.h, this method is renamed <b>MFTSetOutputBounds</b>. See <a href="comparison_of_mfts_and_dmos.htm">Creating Hybrid DMO/MFT Objects</a>.




## -see-also




<a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>
 

 

