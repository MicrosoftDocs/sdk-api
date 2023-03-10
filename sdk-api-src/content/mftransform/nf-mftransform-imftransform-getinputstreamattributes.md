---
UID: NF:mftransform.IMFTransform.GetInputStreamAttributes
title: IMFTransform::GetInputStreamAttributes (mftransform.h)
description: Gets the attribute store for an input stream on this Media Foundation transform (MFT).
helpviewer_keywords: ["2698da30-6913-41a9-9d98-f124cf31e591","GetInputStreamAttributes","GetInputStreamAttributes method [Media Foundation]","GetInputStreamAttributes method [Media Foundation]","IMFTransform interface","IMFTransform interface [Media Foundation]","GetInputStreamAttributes method","IMFTransform.GetInputStreamAttributes","IMFTransform::GetInputStreamAttributes","mf.imftransform_getinputstreamattributes","mftransform/IMFTransform::GetInputStreamAttributes"]
old-location: mf\imftransform_getinputstreamattributes.htm
tech.root: mf
ms.assetid: 2698da30-6913-41a9-9d98-f124cf31e591
ms.date: 12/05/2018
ms.keywords: 2698da30-6913-41a9-9d98-f124cf31e591, GetInputStreamAttributes, GetInputStreamAttributes method [Media Foundation], GetInputStreamAttributes method [Media Foundation],IMFTransform interface, IMFTransform interface [Media Foundation],GetInputStreamAttributes method, IMFTransform.GetInputStreamAttributes, IMFTransform::GetInputStreamAttributes, mf.imftransform_getinputstreamattributes, mftransform/IMFTransform::GetInputStreamAttributes
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
 - IMFTransform::GetInputStreamAttributes
 - mftransform/IMFTransform::GetInputStreamAttributes
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
 - IMFTransform.GetInputStreamAttributes
---

# IMFTransform::GetInputStreamAttributes


## -description

Gets the attribute store for an input stream on this Media Foundation transform (MFT).

## -parameters

### -param dwInputStreamID [in]

Input stream identifier. To get the list of stream identifiers, call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids">IMFTransform::GetStreamIDs</a>.

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
The MFT does not support input stream attributes.
              

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
</table>

## -remarks

Implementation of this method is optional unless the MFT needs to support a particular set of attributes. 

To get the attribute store for the entire MFT, call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes">IMFTransform::GetAttributes</a>.

## -see-also

<a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a>



<a href="/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>



<a href="/windows/desktop/medfound/transform-attributes">Transform Attributes</a>