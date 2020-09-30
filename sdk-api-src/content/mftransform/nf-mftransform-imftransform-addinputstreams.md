---
UID: NF:mftransform.IMFTransform.AddInputStreams
title: IMFTransform::AddInputStreams (mftransform.h)
description: Adds one or more new input streams to this Media Foundation transform (MFT).
helpviewer_keywords: ["311ab66e-5dbd-452a-bad4-99a6293cbc60","AddInputStreams","AddInputStreams method [Media Foundation]","AddInputStreams method [Media Foundation]","IMFTransform interface","IMFTransform interface [Media Foundation]","AddInputStreams method","IMFTransform.AddInputStreams","IMFTransform::AddInputStreams","mf.imftransform_addinputstreams","mftransform/IMFTransform::AddInputStreams"]
old-location: mf\imftransform_addinputstreams.htm
tech.root: mf
ms.assetid: 311ab66e-5dbd-452a-bad4-99a6293cbc60
ms.date: 12/05/2018
ms.keywords: 311ab66e-5dbd-452a-bad4-99a6293cbc60, AddInputStreams, AddInputStreams method [Media Foundation], AddInputStreams method [Media Foundation],IMFTransform interface, IMFTransform interface [Media Foundation],AddInputStreams method, IMFTransform.AddInputStreams, IMFTransform::AddInputStreams, mf.imftransform_addinputstreams, mftransform/IMFTransform::AddInputStreams
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
 - IMFTransform::AddInputStreams
 - mftransform/IMFTransform::AddInputStreams
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
 - IMFTransform.AddInputStreams
---

# IMFTransform::AddInputStreams


## -description

Adds one or more new input streams to this Media Foundation transform (MFT).

## -parameters

### -param cStreams [in]

Number of streams to add.

### -param adwStreamIDs [in]

Array of stream identifiers. The new stream identifiers must not match any existing input streams.

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
Invalid argument.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The MFT has a fixed number of input streams.
              

</td>
</tr>
</table>

## -remarks

If the new streams exceed the maximum number of input streams for this transform, the method returns <b>E_INVALIDARG.</b> To find the maximum number of input streams, call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamlimits">IMFTransform::GetStreamLimits</a>.
      

If any of the new stream identifiers conflicts with an existing input stream, the method returns <b>E_INVALIDARG</b>.
      

If <b>MFT_UNIQUE_METHOD_NAMES</b> is defined before including mftransform.h, this method is renamed <b>MFTAddInputStreams</b>. See <a href="/windows/desktop/medfound/comparison-of-mfts-and-dmos">Creating Hybrid DMO/MFT Objects</a>.

## -see-also

<a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a>



<a href="/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>