---
UID: NF:mftransform.IMFTransform.GetOutputAvailableType
title: IMFTransform::GetOutputAvailableType (mftransform.h)
description: Gets an available media type for an output stream on this Media Foundation transform (MFT).
helpviewer_keywords: ["GetOutputAvailableType","GetOutputAvailableType method [Media Foundation]","GetOutputAvailableType method [Media Foundation]","IMFTransform interface","IMFTransform interface [Media Foundation]","GetOutputAvailableType method","IMFTransform.GetOutputAvailableType","IMFTransform::GetOutputAvailableType","d0f75414-18cf-4e76-b875-5f373510c87b","mf.imftransform_getoutputavailabletype","mftransform/IMFTransform::GetOutputAvailableType"]
old-location: mf\imftransform_getoutputavailabletype.htm
tech.root: mf
ms.assetid: d0f75414-18cf-4e76-b875-5f373510c87b
ms.date: 12/05/2018
ms.keywords: GetOutputAvailableType, GetOutputAvailableType method [Media Foundation], GetOutputAvailableType method [Media Foundation],IMFTransform interface, IMFTransform interface [Media Foundation],GetOutputAvailableType method, IMFTransform.GetOutputAvailableType, IMFTransform::GetOutputAvailableType, d0f75414-18cf-4e76-b875-5f373510c87b, mf.imftransform_getoutputavailabletype, mftransform/IMFTransform::GetOutputAvailableType
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFTransform::GetOutputAvailableType
 - mftransform/IMFTransform::GetOutputAvailableType
dev_langs:
 - c++
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
---

# IMFTransform::GetOutputAvailableType


## -description

Gets an available media type for an output stream on this Media Foundation transform (MFT).

## -parameters

### -param dwOutputStreamID [in]

Output stream identifier. To get the list of stream identifiers, call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids">IMFTransform::GetStreamIDs</a>.

### -param dwTypeIndex [in]

Index of the media type to retrieve. Media types are indexed from zero and returned in approximate order of preference.

### -param ppType [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface. The caller must release the interface.

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
      

Setting the media type on one stream can change the available types for another stream (or change the preference order). However, an MFT is not required to update the list of available types dynamically. The only guaranteed way to test whether you can set a particular input type is to call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype">IMFTransform::SetOutputType</a>.
      

In some cases, an MFT cannot return a list of output types until one or more input types are set. If so, the method returns <b>MF_E_TRANSFORM_TYPE_NOT_SET</b>.
      

An MFT is not required to implement this method. However, most MFTs should implement this method, unless the supported types are simple and can be discovered through the <a href="/windows/desktop/api/mfapi/nf-mfapi-mftgetinfo">MFTGetInfo</a> function.
      

This method can return a <i>partial</i> media type. A partial media type contains an incomplete description of a format, and is used to provide a hint to the caller. For example, a partial type might include just the major type and subtype GUIDs. However, after the client sets the input types on the MFT, the MFT should generally return at least one complete output type, which can be used without further modification.
      For more information, see <a href="/windows/desktop/medfound/complete-and-partial-media-types">Complete and Partial Media Types</a>.

Some MFTs cannot provide an accurate list of output types until the MFT receives the first input sample. For example, the MFT might need to read the first packet header to deduce the format. An MFT should handle this situation as follows:

<ol>
<li>Before the MFT receives any input, it offers a list of one or more output types that it could possibly produce. For example, an MPEG-2 decoder might return a media type that describes the MPEG-2 main profile/main level.
          </li>
<li>The client selects one of these types (generally the first) and sets it on the output stream.
          </li>
<li>The client delivers the first input sample by calling <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput">IMFTransform::ProcessInput</a>.
          </li>
<li>If the output type does not conform to the input data, the transform signals a format change in the <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">ProcessOutput</a> method. For more information about format changes, see <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">IMFTransform::ProcessOutput</a>.
          </li>
<li>The calls <b>GetOutputAvailableType</b> again. At this point, the method should return an updated list of types that reflects the input data.
          </li>
<li>The client selects a new output type from this list and calls <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype">SetOutputType</a>.
          </li>
</ol>
If <b>MFT_UNIQUE_METHOD_NAMES</b> is defined before including mftransform.h, this method is renamed <b>MFTGetOutputAvailableType</b>. See <a href="/windows/desktop/medfound/comparison-of-mfts-and-dmos">Creating Hybrid DMO/MFT Objects</a>.

<h3><a id="Implementation_Notes"></a><a id="implementation_notes"></a><a id="IMPLEMENTATION_NOTES"></a>Implementation Notes</h3>
If the MFT stores a media type internally, the MFT should return a clone of the media  type, not a pointer to the original type. Otherwise, the caller might modify the type and alter the internal state of the MFT.

## -see-also

<a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a>



<a href="/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>