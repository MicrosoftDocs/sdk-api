---
UID: NF:mftransform.IMFTransform.GetOutputAvailableType
title: IMFTransform::GetOutputAvailableType
author: windows-sdk-content
description: Gets an available media type for an output stream on this Media Foundation transform (MFT).
old-location: mf\imftransform_getoutputavailabletype.htm
old-project: medfound
ms.assetid: d0f75414-18cf-4e76-b875-5f373510c87b
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetOutputAvailableType, GetOutputAvailableType method [Media Foundation], GetOutputAvailableType method [Media Foundation],IMFTransform interface, IMFTransform interface [Media Foundation],GetOutputAvailableType method, IMFTransform.GetOutputAvailableType, IMFTransform::GetOutputAvailableType, d0f75414-18cf-4e76-b875-5f373510c87b, mf.imftransform_getoutputavailabletype, mftransform/IMFTransform::GetOutputAvailableType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mftransform.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFTransform.GetOutputAvailableType
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTransform::GetOutputAvailableType


## -description


Gets an available media type for an output stream on this Media Foundation transform (MFT).
        


## -parameters




### -param dwOutputStreamID [in]

Output stream identifier. To get the list of stream identifiers, call <a href="https://msdn.microsoft.com/0715c78e-de92-439d-a4f3-078e19f78a8e">IMFTransform::GetStreamIDs</a>.
          


### -param dwTypeIndex [in]

Index of the media type to retrieve. Media types are indexed from zero and returned in approximate order of preference.
          


### -param ppType [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface. The caller must release the interface.
          


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
The MFT does not have a list of available output types.
              

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
<dt><b>MF_E_NO_MORE_TYPES</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwTypeIndex</i> parameter is out of range.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_TRANSFORM_TYPE_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
You must set the input types before setting the output types.
              

</td>
</tr>
</table>
 




## -remarks



The MFT defines a list of available media types for each output stream and orders them by preference. This method enumerates the available media types for an output stream. To enumerate the available types, increment <i>dwTypeIndex</i> until the method returns MF_<b>E_NO_MORE_TYPES</b>.
      

Setting the media type on one stream can change the available types for another stream (or change the preference order). However, an MFT is not required to update the list of available types dynamically. The only guaranteed way to test whether you can set a particular input type is to call <a href="https://msdn.microsoft.com/a9a1d03f-2e56-490c-885b-78c69dea8e92">IMFTransform::SetOutputType</a>.
      

In some cases, an MFT cannot return a list of output types until one or more input types are set. If so, the method returns <b>MF_E_TRANSFORM_TYPE_NOT_SET</b>.
      

An MFT is not required to implement this method. However, most MFTs should implement this method, unless the supported types are simple and can be discovered through the <a href="https://msdn.microsoft.com/d1bac1c7-3f9b-46b7-bdf7-c32983c648ee">MFTGetInfo</a> function.
      

This method can return a <i>partial</i> media type. A partial media type contains an incomplete description of a format, and is used to provide a hint to the caller. For example, a partial type might include just the major type and subtype GUIDs. However, after the client sets the input types on the MFT, the MFT should generally return at least one complete output type, which can be used without further modification.
      For more information, see <a href="https://msdn.microsoft.com/59b3f0b5-f378-41e6-9b49-85a16bb6e008">Complete and Partial Media Types</a>.

Some MFTs cannot provide an accurate list of output types until the MFT receives the first input sample. For example, the MFT might need to read the first packet header to deduce the format. An MFT should handle this situation as follows:

<ol>
<li>Before the MFT receives any input, it offers a list of one or more output types that it could possibly produce. For example, an MPEG-2 decoder might return a media type that describes the MPEG-2 main profile/main level.
          </li>
<li>The client selects one of these types (generally the first) and sets it on the output stream.
          </li>
<li>The client delivers the first input sample by calling <a href="https://msdn.microsoft.com/c94d406b-7cd9-42d4-ae9e-3d21dbb47209">IMFTransform::ProcessInput</a>.
          </li>
<li>If the output type does not conform to the input data, the transform signals a format change in the <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">ProcessOutput</a> method. For more information about format changes, see <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">IMFTransform::ProcessOutput</a>.
          </li>
<li>The calls <b>GetOutputAvailableType</b> again. At this point, the method should return an updated list of types that reflects the input data.
          </li>
<li>The client selects a new output type from this list and calls <a href="https://msdn.microsoft.com/a9a1d03f-2e56-490c-885b-78c69dea8e92">SetOutputType</a>.
          </li>
</ol>
If <b>MFT_UNIQUE_METHOD_NAMES</b> is defined before including mftransform.h, this method is renamed <b>MFTGetOutputAvailableType</b>. See <a href="comparison_of_mfts_and_dmos.htm">Creating Hybrid DMO/MFT Objects</a>.

<h3><a id="Implementation_Notes"></a><a id="implementation_notes"></a><a id="IMPLEMENTATION_NOTES"></a>Implementation Notes</h3>
If the MFT stores a media type internally, the MFT should return a clone of the media  type, not a pointer to the original type. Otherwise, the caller might modify the type and alter the internal state of the MFT.




## -see-also




<a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>
 

 

