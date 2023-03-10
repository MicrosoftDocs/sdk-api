---
UID: NF:wmdxva.IWMCodecAMVideoAccelerator.NegotiateConnection
title: IWMCodecAMVideoAccelerator::NegotiateConnection (wmdxva.h)
description: The NegotiateConnection method is called by the output pin on the player's source filter during the connection process when it has been given a DirectX VA media type.
helpviewer_keywords: ["IWMCodecAMVideoAccelerator interface [windows Media Format]","NegotiateConnection method","IWMCodecAMVideoAccelerator.NegotiateConnection","IWMCodecAMVideoAccelerator::NegotiateConnection","IWMCodecAMVideoAcceleratorNegotiateConnection","NegotiateConnection","NegotiateConnection method [windows Media Format]","NegotiateConnection method [windows Media Format]","IWMCodecAMVideoAccelerator interface","wmdxva/IWMCodecAMVideoAccelerator::NegotiateConnection","wmformat.iwmcodecamvideoaccelerator_negotiateconnection"]
old-location: wmformat\iwmcodecamvideoaccelerator_negotiateconnection.htm
tech.root: wmformat
ms.assetid: 547c43ed-7e04-4323-9e10-019ecfdbb641
ms.date: 12/05/2018
ms.keywords: IWMCodecAMVideoAccelerator interface [windows Media Format],NegotiateConnection method, IWMCodecAMVideoAccelerator.NegotiateConnection, IWMCodecAMVideoAccelerator::NegotiateConnection, IWMCodecAMVideoAcceleratorNegotiateConnection, NegotiateConnection, NegotiateConnection method [windows Media Format], NegotiateConnection method [windows Media Format],IWMCodecAMVideoAccelerator interface, wmdxva/IWMCodecAMVideoAccelerator::NegotiateConnection, wmformat.iwmcodecamvideoaccelerator_negotiateconnection
req.header: wmdxva.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMCodecAMVideoAccelerator::NegotiateConnection
 - wmdxva/IWMCodecAMVideoAccelerator::NegotiateConnection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMCodecAMVideoAccelerator.NegotiateConnection
---

# IWMCodecAMVideoAccelerator::NegotiateConnection


## -description

The <b>NegotiateConnection</b> method is called by the output pin on the player's source filter during the connection process when it has been given a DirectX VA media type.

## -parameters

### -param pMediaType [in]

Pointer to the media type structure that represents the media type being proposed for the connection.

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
<dt><b>DMO_E_TYPE_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
No input type has been set on the decoder.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The decoder has no valid <b>IAMVideoAccelerator</b> interface pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pMediaType</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/wmformat/enabling-directx-video-acceleration">Enabling DirectX Video Acceleration</a>



<a href="/windows/desktop/api/wmdxva/nn-wmdxva-iwmcodecamvideoaccelerator">IWMCodecAMVideoAccelerator Interface</a>