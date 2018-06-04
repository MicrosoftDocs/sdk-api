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

# IMFTransform::GetStreamIDs


## -description



          Gets the stream identifiers for the input and output streams on this Media Foundation transform (MFT).
        


## -parameters




### -param dwInputIDArraySize [in]


            Number of elements in the <i>pdwInputIDs</i> array.
          


### -param pdwInputIDs [out]


            Pointer to an array allocated by the caller. The method fills the array with the input stream identifiers. The array size must be at least equal to the number of input streams. To get the number of input streams, call <a href="https://msdn.microsoft.com/491f7f44-fcac-4236-ba5c-e5705267c6c2">IMFTransform::GetStreamCount</a>.
          

If the caller passes an array that is larger than the number of input streams, the MFT must not write values into the extra array entries.


### -param dwOutputIDArraySize [in]


            Number of elements in the <i>pdwOutputIDs</i> array.
          


### -param pdwOutputIDs [out]


            Pointer to an array allocated by the caller. The method fills the array with the output stream identifiers. The array size must be at least equal to the number of output streams. To get the number of output streams, call <a href="https://msdn.microsoft.com/491f7f44-fcac-4236-ba5c-e5705267c6c2">GetStreamCount</a>.
          

If the caller passes an array that is larger than the number of output streams, the MFT must not write values into the extra array entries.


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

                Not implemented. See Remarks.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">

                One or both of the arrays is too small.
              

</td>
</tr>
</table>
 




## -remarks




        Stream identifiers are necessary because some MFTs can add or remove streams, so the index of a stream may not be unique. Therefore, <a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a> methods that operate on streams take stream identifiers.
      

This method can return <b>E_NOTIMPL</b> if both of the following conditions are true:

<ul>
<li>
            The transform has a fixed number of streams.
          </li>
<li>
            The streams are numbered consecutively from 0 to n – 1, where n is the number of input streams or output streams. In other words, the first input stream is 0, the second is 1, and so on; and the first output stream is 0, the second is 1, and so on.
          </li>
</ul>
This method must be implemented if any of the following conditions is true:

<ul>
<li>
            The MFT can add or remove output streams.
          </li>
<li>
            The MFT allows the client to add or remove input streams.
          </li>
<li>
            The stream identifiers are not consecutive.
          </li>
</ul>

        All input stream identifiers must be unique within an MFT, and all output stream identifiers must be unique. However, an input stream and an output stream can share the same identifier.
      


        If the client adds an input stream, the client assigns the identifier, so the MFT must allow arbitrary identifiers, as long as they are unique. If the MFT creates an output stream, the MFT assigns the identifier.
      


        By convention, if an MFT has exactly one fixed input stream and one fixed output stream, it should assign the identifier 0 to both streams.
      

If <b>MFT_UNIQUE_METHOD_NAMES</b> is defined before including mftransform.h, this method is renamed <b>MFTGetStreamIDs</b>. See <a href="comparison_of_mfts_and_dmos.htm">Creating Hybrid DMO/MFT Objects</a>.




## -see-also




<a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>
 

 

