---
UID: NF:mftransform.IMFTransform.GetStreamIDs
title: IMFTransform::GetStreamIDs (mftransform.h)
description: Gets the stream identifiers for the input and output streams on this Media Foundation transform (MFT).
helpviewer_keywords: ["0715c78e-de92-439d-a4f3-078e19f78a8e","GetStreamIDs","GetStreamIDs method [Media Foundation]","GetStreamIDs method [Media Foundation]","IMFTransform interface","IMFTransform interface [Media Foundation]","GetStreamIDs method","IMFTransform.GetStreamIDs","IMFTransform::GetStreamIDs","mf.imftransform_getstreamids","mftransform/IMFTransform::GetStreamIDs"]
old-location: mf\imftransform_getstreamids.htm
tech.root: mf
ms.assetid: 0715c78e-de92-439d-a4f3-078e19f78a8e
ms.date: 12/05/2018
ms.keywords: 0715c78e-de92-439d-a4f3-078e19f78a8e, GetStreamIDs, GetStreamIDs method [Media Foundation], GetStreamIDs method [Media Foundation],IMFTransform interface, IMFTransform interface [Media Foundation],GetStreamIDs method, IMFTransform.GetStreamIDs, IMFTransform::GetStreamIDs, mf.imftransform_getstreamids, mftransform/IMFTransform::GetStreamIDs
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
 - IMFTransform::GetStreamIDs
 - mftransform/IMFTransform::GetStreamIDs
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
 - IMFTransform.GetStreamIDs
---

# IMFTransform::GetStreamIDs


## -description

Gets the stream identifiers for the input and output streams on this Media Foundation transform (MFT).

## -parameters

### -param dwInputIDArraySize [in]

Number of elements in the <i>pdwInputIDs</i> array.

### -param pdwInputIDs [out]

Pointer to an array allocated by the caller. The method fills the array with the input stream identifiers. The array size must be at least equal to the number of input streams. To get the number of input streams, call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount">IMFTransform::GetStreamCount</a>.
          

If the caller passes an array that is larger than the number of input streams, the MFT must not write values into the extra array entries.

### -param dwOutputIDArraySize [in]

Number of elements in the <i>pdwOutputIDs</i> array.

### -param pdwOutputIDs [out]

Pointer to an array allocated by the caller. The method fills the array with the output stream identifiers. The array size must be at least equal to the number of output streams. To get the number of output streams, call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount">GetStreamCount</a>.
          

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

Stream identifiers are necessary because some MFTs can add or remove streams, so the index of a stream may not be unique. Therefore, <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a> methods that operate on streams take stream identifiers.
      

This method can return <b>E_NOTIMPL</b> if both of the following conditions are true:

<ul>
<li>The transform has a fixed number of streams.
          </li>
<li>The streams are numbered consecutively from 0 to n – 1, where n is the number of input streams or output streams. In other words, the first input stream is 0, the second is 1, and so on; and the first output stream is 0, the second is 1, and so on.
          </li>
</ul>
This method must be implemented if any of the following conditions is true:

<ul>
<li>The MFT can add or remove output streams.
          </li>
<li>The MFT allows the client to add or remove input streams.
          </li>
<li>The stream identifiers are not consecutive.
          </li>
</ul>
All input stream identifiers must be unique within an MFT, and all output stream identifiers must be unique. However, an input stream and an output stream can share the same identifier.
      

If the client adds an input stream, the client assigns the identifier, so the MFT must allow arbitrary identifiers, as long as they are unique. If the MFT creates an output stream, the MFT assigns the identifier.
      

By convention, if an MFT has exactly one fixed input stream and one fixed output stream, it should assign the identifier 0 to both streams.
      

If <b>MFT_UNIQUE_METHOD_NAMES</b> is defined before including mftransform.h, this method is renamed <b>MFTGetStreamIDs</b>. See <a href="/windows/desktop/medfound/comparison-of-mfts-and-dmos">Creating Hybrid DMO/MFT Objects</a>.

## -see-also

<a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a>



<a href="/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>