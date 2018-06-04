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

# IMFTransform::GetInputStatus


## -description



          Queries whether an input stream on this Media Foundation transform (MFT) can accept more data.
        


## -parameters




### -param dwInputStreamID [in]


            Input stream identifier. To get the list of stream identifiers, call <a href="https://msdn.microsoft.com/0715c78e-de92-439d-a4f3-078e19f78a8e">IMFTransform::GetStreamIDs</a>.
          


### -param pdwFlags [out]


            Receives a member of the <a href="https://msdn.microsoft.com/c63052a1-58b6-4537-9214-6f8d79a9eafd">_MFT_INPUT_STATUS_FLAGS</a> enumeration, or zero. If the value is <b>MFT_INPUT_STATUS_ACCEPT_DATA</b>, the stream specified in <i>dwInputStreamID</i> can accept more input data.
          


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
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">

                Invalid stream identifier.
              

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




        If the method returns the <b>MFT_INPUT_STATUS_ACCEPT_DATA</b> flag, you can deliver an input sample to the specified stream by calling <a href="https://msdn.microsoft.com/c94d406b-7cd9-42d4-ae9e-3d21dbb47209">IMFTransform::ProcessInput</a>. If the method succeeds but does not return any flags in the <i>pdwFlags</i> parameter, it means the input stream already has as much data as it can accept.
      


        Use this method to test whether the input stream is ready to accept more data, without incurring the overhead of allocating a new sample and calling <a href="https://msdn.microsoft.com/c94d406b-7cd9-42d4-ae9e-3d21dbb47209">ProcessInput</a>.
      


        After the client has set valid media types on all of the streams, the MFT should always be in one of two states: Able to accept more input, or able to produce more output (or both).
      

If <b>MFT_UNIQUE_METHOD_NAMES</b> is defined before including mftransform.h, this method is renamed <b>MFTGetInputStatus</b>. See <a href="comparison_of_mfts_and_dmos.htm">Creating Hybrid DMO/MFT Objects</a>.




## -see-also




<a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>
 

 

