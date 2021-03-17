---
UID: NF:mftransform.IMFTransform.GetAttributes
title: IMFTransform::GetAttributes (mftransform.h)
description: Gets the global attribute store for this Media Foundation transform (MFT).
helpviewer_keywords: ["GetAttributes","GetAttributes method [Media Foundation]","GetAttributes method [Media Foundation]","IMFTransform interface","IMFTransform interface [Media Foundation]","GetAttributes method","IMFTransform.GetAttributes","IMFTransform::GetAttributes","cb3ba2bc-550c-43b4-a69c-b546f2b92acc","mf.imftransform_getattributes","mftransform/IMFTransform::GetAttributes"]
old-location: mf\imftransform_getattributes.htm
tech.root: mf
ms.assetid: cb3ba2bc-550c-43b4-a69c-b546f2b92acc
ms.date: 12/05/2018
ms.keywords: GetAttributes, GetAttributes method [Media Foundation], GetAttributes method [Media Foundation],IMFTransform interface, IMFTransform interface [Media Foundation],GetAttributes method, IMFTransform.GetAttributes, IMFTransform::GetAttributes, cb3ba2bc-550c-43b4-a69c-b546f2b92acc, mf.imftransform_getattributes, mftransform/IMFTransform::GetAttributes
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
 - IMFTransform::GetAttributes
 - mftransform/IMFTransform::GetAttributes
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
 - IMFTransform.GetAttributes
---

# IMFTransform::GetAttributes


## -description

Gets the global attribute store for this Media Foundation transform (MFT).

## -parameters

### -param pAttributes [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface. The caller must release the interface.

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
The MFT does not support attributes.
              

</td>
</tr>
</table>

## -remarks

Use the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> pointer retrieved by this method to get or set attributes that apply to the entire MFT. To get the attribute store for an input stream, call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes">IMFTransform::GetInputStreamAttributes</a>. To get the attribute store for an output stream, call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes">IMFTransform::GetOutputStreamAttributes</a>.
      

Implementation of this method is optional unless the MFT needs to support a particular set of attributes. Exception: Hardware-based MFTs must implement this method. See <a href="/windows/desktop/medfound/hardware-mfts">Hardware MFTs</a>.

## -see-also

<a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a>



<a href="/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>



<a href="/windows/desktop/medfound/transform-attributes">Transform Attributes</a>