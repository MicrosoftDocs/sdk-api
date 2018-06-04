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

# IMFTransform::GetOutputStatus


## -description



          Queries whether the Media Foundation transform (MFT) is ready to produce output data.
        


## -parameters




### -param pdwFlags [out]


            Receives a member of the <a href="https://msdn.microsoft.com/951900b1-364e-4867-a1f8-50d485d13c77">_MFT_OUTPUT_STATUS_FLAGS</a> enumeration, or zero. If the value is <b>MFT_OUTPUT_STATUS_SAMPLE_READY</b>, the MFT can produce an output sample.
          


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




        If the method returns the <b>MFT_OUTPUT_STATUS_SAMPLE_READY</b> flag, it means you can generate one or more output samples by calling <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">IMFTransform::ProcessOutput</a>.
      


        MFTs are not required to implement this method. If the method returns <b>E_NOTIMPL</b>, you must call <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">ProcessOutput</a> to determine whether the transform has output data.
      


        If the MFT has more than one output stream, but it does not produce samples at the same time for each stream, it can set the <b>MFT_OUTPUT_STATUS_SAMPLE_READY</b> flag when just one stream is ready. However, if the MFT normally produces samples at the same time for each output stream, it should not set this flag until all streams are ready.
      


        After the client has set valid media types on all of the streams, the MFT should always be in one of two states: Able to accept more input, or able to produce more output.
      

If <b>MFT_UNIQUE_METHOD_NAMES</b> is defined before including mftransform.h, this method is renamed <b>MFTGetOutputStatus</b>. See <a href="comparison_of_mfts_and_dmos.htm">Creating Hybrid DMO/MFT Objects</a>.




## -see-also




<a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>
 

 

