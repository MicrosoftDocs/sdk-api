---
UID: NF:videoacc.IAMVideoAccelerator.GetInternalMemInfo
title: IAMVideoAccelerator::GetInternalMemInfo (videoacc.h)
description: The GetInternalMemInfo method queries for the amount of scratch memory the hardware abstraction layer (HAL) will allocate for its private use.
helpviewer_keywords: ["GetInternalMemInfo","GetInternalMemInfo method [DirectShow]","GetInternalMemInfo method [DirectShow]","IAMVideoAccelerator interface","IAMVideoAccelerator interface [DirectShow]","GetInternalMemInfo method","IAMVideoAccelerator.GetInternalMemInfo","IAMVideoAccelerator::GetInternalMemInfo","IAMVideoAcceleratorGetInternalMemInfo","dshow.iamvideoaccelerator_getinternalmeminfo","videoacc/IAMVideoAccelerator::GetInternalMemInfo"]
old-location: dshow\iamvideoaccelerator_getinternalmeminfo.htm
tech.root: dshow
ms.assetid: 64b6371c-4baf-4ec1-bd0d-6413f053e2fa
ms.date: 12/05/2018
ms.keywords: GetInternalMemInfo, GetInternalMemInfo method [DirectShow], GetInternalMemInfo method [DirectShow],IAMVideoAccelerator interface, IAMVideoAccelerator interface [DirectShow],GetInternalMemInfo method, IAMVideoAccelerator.GetInternalMemInfo, IAMVideoAccelerator::GetInternalMemInfo, IAMVideoAcceleratorGetInternalMemInfo, dshow.iamvideoaccelerator_getinternalmeminfo, videoacc/IAMVideoAccelerator::GetInternalMemInfo
req.header: videoacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMVideoAccelerator::GetInternalMemInfo
 - videoacc/IAMVideoAccelerator::GetInternalMemInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMVideoAccelerator.GetInternalMemInfo
---

# IAMVideoAccelerator::GetInternalMemInfo


## -description

The <b>GetInternalMemInfo</b> method queries for the amount of scratch memory the hardware abstraction layer (HAL) will allocate for its private use.

## -parameters

### -param pGuid [in]

Pointer to a GUID that specifies the DXVA profile in use.

### -param pamvaUncompDataInfo [in]

Pointer to an <a href="/previous-versions/windows/desktop/api/amva/ns-amva-amvauncompdatainfo">AMVAUncompDataInfo</a> structure that specifies the size and pixel format of the uncompressed data.

### -param pamvaInternalMemInfo [in, out]

Pointer to an <a href="/previous-versions/windows/desktop/api/amva/ns-amva-amvainternalmeminfo">AMVAInternalMemInfo</a> structure that receives the amount of scratch memory the HAL will allocate.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface. <b>HRESULT</b> can include one of the following standard constants, or other values not listed.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Argument is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/DirectShow/how-decoders-use-iamvideoaccelerator">How Decoders Use IAMVideoAccelerator</a>



<a href="/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator">IAMVideoAccelerator Interface</a>