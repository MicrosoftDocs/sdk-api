---
UID: NF:mftransform.IMFTransform.DeleteInputStream
title: IMFTransform::DeleteInputStream (mftransform.h)
description: Removes an input stream from this Media Foundation transform (MFT).
helpviewer_keywords: ["DeleteInputStream","DeleteInputStream method [Media Foundation]","DeleteInputStream method [Media Foundation]","IMFTransform interface","IMFTransform interface [Media Foundation]","DeleteInputStream method","IMFTransform.DeleteInputStream","IMFTransform::DeleteInputStream","cba37f7f-6ab2-469c-95c2-61d9e4d31d0b","mf.imftransform_deleteinputstream","mftransform/IMFTransform::DeleteInputStream"]
old-location: mf\imftransform_deleteinputstream.htm
tech.root: mf
ms.assetid: cba37f7f-6ab2-469c-95c2-61d9e4d31d0b
ms.date: 12/05/2018
ms.keywords: DeleteInputStream, DeleteInputStream method [Media Foundation], DeleteInputStream method [Media Foundation],IMFTransform interface, IMFTransform interface [Media Foundation],DeleteInputStream method, IMFTransform.DeleteInputStream, IMFTransform::DeleteInputStream, cba37f7f-6ab2-469c-95c2-61d9e4d31d0b, mf.imftransform_deleteinputstream, mftransform/IMFTransform::DeleteInputStream
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
 - IMFTransform::DeleteInputStream
 - mftransform/IMFTransform::DeleteInputStream
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
 - IMFTransform.DeleteInputStream
---

# IMFTransform::DeleteInputStream


## -description

Removes an input stream from this Media Foundation transform (MFT).

## -parameters

### -param dwStreamID [in]

Identifier of the input stream to remove.

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
The transform has a fixed number of input streams.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The stream is not removable, or the transform currently has the minimum number of input streams it can support.
              

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
<dt><b>MF_E_TRANSFORM_INPUT_REMAINING</b></dt>
</dl>
</td>
<td width="60%">
The transform has unprocessed input buffers for the specified stream.
              

</td>
</tr>
</table>

## -remarks

If the transform has a fixed number of input streams, the method returns <b>E_NOTIMPL</b>.
      

An MFT might support this method but not allow certain input streams to be removed. If an input stream can be removed, the <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo">IMFTransform::GetInputStreamInfo</a> method returns the <b>MFT_INPUT_STREAM_REMOVABLE</b> flag for that stream. Otherwise, the stream cannot be removed, and the method returns <b>MF_E_INVALIDREQUEST</b>. The method also fails if the MFT currently has the minimum number of input streams that it requires. To find the minimum number of streams, call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamlimits">IMFTransform::GetStreamLimits</a>.
      

If the transform still has unprocessed input for that stream, the method might succeed or it might return <b>MF_E_TRANSFORM_INPUT_REMAINING</b>. If the method succeeds, the MFT will continue to process the remaining input after the stream is removed. If the method returns <b>MF_E_TRANSFORM_INPUT_REMAINING</b>, you must clear the input buffers before removing the stream. To clear the input buffers, either call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">IMFTransform::ProcessOutput</a> or else call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage">IMFTransform::ProcessMessage</a> with the <b>MFT_MESSAGE_COMMAND_FLUSH</b> to flush the MFT. Then call the <b>DeleteInputStream</b> again. An MFT should never discard input buffers when <b>DeleteInputStream</b> is called.
      

If <b>MFT_UNIQUE_METHOD_NAMES</b> is defined before including mftransform.h, this method is renamed <b>MFTDeleteInputStream</b>. See <a href="/windows/desktop/medfound/comparison-of-mfts-and-dmos">Creating Hybrid DMO/MFT Objects</a>.

## -see-also

<a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a>



<a href="/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>