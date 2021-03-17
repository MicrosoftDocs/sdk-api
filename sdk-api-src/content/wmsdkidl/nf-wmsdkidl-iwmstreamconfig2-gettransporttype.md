---
UID: NF:wmsdkidl.IWMStreamConfig2.GetTransportType
title: IWMStreamConfig2::GetTransportType (wmsdkidl.h)
description: The GetTransportType method retrieves the type of data communication protocol (reliable or unreliable) used for the stream.
helpviewer_keywords: ["GetTransportType","GetTransportType method [windows Media Format]","GetTransportType method [windows Media Format]","IWMStreamConfig2 interface","IWMStreamConfig2 interface [windows Media Format]","GetTransportType method","IWMStreamConfig2.GetTransportType","IWMStreamConfig2::GetTransportType","IWMStreamConfig2GetTransportType","wmformat.iwmstreamconfig2_gettransporttype","wmsdkidl/IWMStreamConfig2::GetTransportType"]
old-location: wmformat\iwmstreamconfig2_gettransporttype.htm
tech.root: wmformat
ms.assetid: dfe7b285-8d1d-4b71-a839-1c73d76e6444
ms.date: 12/05/2018
ms.keywords: GetTransportType, GetTransportType method [windows Media Format], GetTransportType method [windows Media Format],IWMStreamConfig2 interface, IWMStreamConfig2 interface [windows Media Format],GetTransportType method, IWMStreamConfig2.GetTransportType, IWMStreamConfig2::GetTransportType, IWMStreamConfig2GetTransportType, wmformat.iwmstreamconfig2_gettransporttype, wmsdkidl/IWMStreamConfig2::GetTransportType
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMStreamConfig2::GetTransportType
 - wmsdkidl/IWMStreamConfig2::GetTransportType
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
 - IWMStreamConfig2.GetTransportType
---

# IWMStreamConfig2::GetTransportType


## -description

The <b>GetTransportType</b> method retrieves the type of data communication protocol (reliable or unreliable) used for the stream.

## -parameters

### -param pnTransportType [out]

Pointer to a variable that receives one member of the <a href="/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_transport_type">WMT_TRANSPORT_TYPE</a> enumeration type.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pnTransportType</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2">IWMStreamConfig2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-settransporttype">IWMStreamConfig2::SetTransportType</a>