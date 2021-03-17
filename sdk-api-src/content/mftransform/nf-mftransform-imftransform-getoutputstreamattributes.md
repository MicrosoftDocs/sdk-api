---
UID: NF:mftransform.IMFTransform.GetOutputStreamAttributes
title: IMFTransform::GetOutputStreamAttributes (mftransform.h)
description: Gets the attribute store for an output stream on this Media Foundation transform (MFT).
helpviewer_keywords: ["GetOutputStreamAttributes","GetOutputStreamAttributes method [Media Foundation]","GetOutputStreamAttributes method [Media Foundation]","IMFTransform interface","IMFTransform interface [Media Foundation]","GetOutputStreamAttributes method","IMFTransform.GetOutputStreamAttributes","IMFTransform::GetOutputStreamAttributes","d54ce20c-8ef9-4480-9ddd-908751fc0a7e","mf.imftransform_getoutputstreamattributes","mftransform/IMFTransform::GetOutputStreamAttributes"]
old-location: mf\imftransform_getoutputstreamattributes.htm
tech.root: mf
ms.assetid: d54ce20c-8ef9-4480-9ddd-908751fc0a7e
ms.date: 12/05/2018
ms.keywords: GetOutputStreamAttributes, GetOutputStreamAttributes method [Media Foundation], GetOutputStreamAttributes method [Media Foundation],IMFTransform interface, IMFTransform interface [Media Foundation],GetOutputStreamAttributes method, IMFTransform.GetOutputStreamAttributes, IMFTransform::GetOutputStreamAttributes, d54ce20c-8ef9-4480-9ddd-908751fc0a7e, mf.imftransform_getoutputstreamattributes, mftransform/IMFTransform::GetOutputStreamAttributes
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
 - IMFTransform::GetOutputStreamAttributes
 - mftransform/IMFTransform::GetOutputStreamAttributes
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
 - IMFTransform.GetOutputStreamAttributes
---

# IMFTransform::GetOutputStreamAttributes


## -description

Gets the attribute store for an output stream on this Media Foundation transform (MFT).

## -parameters

### -param dwOutputStreamID [in]

Output stream identifier. To get the list of stream identifiers, call <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids">IMFTransform::GetStreamIDs</a>.

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
The MFT does not support output stream attributes.
              

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