---
UID: NF:mfapi.MFCreateLegacyMediaBufferOnMFMediaBuffer
title: MFCreateLegacyMediaBufferOnMFMediaBuffer function (mfapi.h)
description: Converts a Media Foundation media buffer into a buffer that is compatible with DirectX Media Objects (DMOs).
helpviewer_keywords: ["35d749d8-2bca-4fe8-b145-175e178ae529","MFCreateLegacyMediaBufferOnMFMediaBuffer","MFCreateLegacyMediaBufferOnMFMediaBuffer function [Media Foundation]","mf.mfcreatelegacymediabufferonmfmediabuffer","mfapi/MFCreateLegacyMediaBufferOnMFMediaBuffer"]
old-location: mf\mfcreatelegacymediabufferonmfmediabuffer.htm
tech.root: mf
ms.assetid: 35d749d8-2bca-4fe8-b145-175e178ae529
ms.date: 12/05/2018
ms.keywords: 35d749d8-2bca-4fe8-b145-175e178ae529, MFCreateLegacyMediaBufferOnMFMediaBuffer, MFCreateLegacyMediaBufferOnMFMediaBuffer function [Media Foundation], mf.mfcreatelegacymediabufferonmfmediabuffer, mfapi/MFCreateLegacyMediaBufferOnMFMediaBuffer
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateLegacyMediaBufferOnMFMediaBuffer
 - mfapi/MFCreateLegacyMediaBufferOnMFMediaBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateLegacyMediaBufferOnMFMediaBuffer
---

# MFCreateLegacyMediaBufferOnMFMediaBuffer function


## -description

Converts a Media Foundation media buffer into a buffer that is compatible with DirectX Media Objects (DMOs).

## -parameters

### -param pSample

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> interface of the sample that contains the Media Foundation buffer. This parameter can be <b>NULL</b>.

### -param pMFMediaBuffer

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a> interface of the Media Foundation buffer.

### -param cbOffset

Offset in bytes from the start of the Media Foundation buffer. This offset defines where the DMO buffer starts. If this parameter is zero, the DMO buffer starts at the beginning of the Media Foundation buffer.

### -param ppMediaBuffer

Receives a pointer to the <b>IMediaBuffer</b> interface. This interface is documented in the DirectShow SDK documentation. The caller must release the interface.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument. The <i>pIMFMediaBuffer</i> parameter must not be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The DMO buffer created by this function also exposes the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> interface. If <i>pIMFSample</i> is <b>NULL</b>, all of the <b>IMFSample</b> methods return MF_E_NOT_INITIALIZED. Otherwise, they call through to the <i>pIMFSample</i> pointer.

If the Media Foundation buffer specified by <i>pIMFMediaBuffer</i> exposes the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer">IMF2DBuffer</a> interface, the DMO buffer also exposes <b>IMF2DBuffer</b>.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer">IMF2DBuffer</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a>



<a href="/windows/desktop/medfound/media-buffers">Media Buffers</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>