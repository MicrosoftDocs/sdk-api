---
UID: NF:wmsdkidl.IWMStreamConfig.GetBufferWindow
title: IWMStreamConfig::GetBufferWindow (wmsdkidl.h)
description: The GetBufferWindow method retrieves the maximum latency between when a stream is received and when it begins to be displayed.
helpviewer_keywords: ["GetBufferWindow","GetBufferWindow method [windows Media Format]","GetBufferWindow method [windows Media Format]","IWMStreamConfig interface","IWMStreamConfig interface [windows Media Format]","GetBufferWindow method","IWMStreamConfig.GetBufferWindow","IWMStreamConfig::GetBufferWindow","IWMStreamConfigGetBufferWindow","wmformat.iwmstreamconfig_getbufferwindow","wmsdkidl/IWMStreamConfig::GetBufferWindow"]
old-location: wmformat\iwmstreamconfig_getbufferwindow.htm
tech.root: wmformat
ms.assetid: 7a78cd61-e7ae-42e2-9d64-f3344fefc59d
ms.date: 12/05/2018
ms.keywords: GetBufferWindow, GetBufferWindow method [windows Media Format], GetBufferWindow method [windows Media Format],IWMStreamConfig interface, IWMStreamConfig interface [windows Media Format],GetBufferWindow method, IWMStreamConfig.GetBufferWindow, IWMStreamConfig::GetBufferWindow, IWMStreamConfigGetBufferWindow, wmformat.iwmstreamconfig_getbufferwindow, wmsdkidl/IWMStreamConfig::GetBufferWindow
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
 - IWMStreamConfig::GetBufferWindow
 - wmsdkidl/IWMStreamConfig::GetBufferWindow
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
 - IWMStreamConfig.GetBufferWindow
---

# IWMStreamConfig::GetBufferWindow


## -description

The <b>GetBufferWindow</b> method retrieves the maximum latency between when a stream is received and when it begins to be displayed.

## -parameters

### -param pmsBufferWindow [out]

Pointer to a variable specifying the buffer window, in milliseconds.

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
The <i>pmsBufferWindow</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig">IWMStreamConfig Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow">IWMStreamConfig::SetBufferWindow</a>