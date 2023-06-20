---
UID: NF:wmsdkidl.IWMProfile.RemoveStream
title: IWMProfile::RemoveStream (wmsdkidl.h)
description: The RemoveStream method removes a stream from the profile.
helpviewer_keywords: ["IWMProfile interface [windows Media Format]","RemoveStream method","IWMProfile.RemoveStream","IWMProfile2 interface [windows Media Format]","RemoveStream method","IWMProfile2::RemoveStream","IWMProfile3 interface [windows Media Format]","RemoveStream method","IWMProfile3::RemoveStream","IWMProfile::RemoveStream","IWMProfileRemoveStream","RemoveStream","RemoveStream method [windows Media Format]","RemoveStream method [windows Media Format]","IWMProfile interface","RemoveStream method [windows Media Format]","IWMProfile2 interface","RemoveStream method [windows Media Format]","IWMProfile3 interface","wmformat.iwmprofile_removestream","wmsdkidl/IWMProfile2::RemoveStream","wmsdkidl/IWMProfile3::RemoveStream","wmsdkidl/IWMProfile::RemoveStream"]
old-location: wmformat\iwmprofile_removestream.htm
tech.root: wmformat
ms.assetid: 82817b72-fde5-492e-b197-87bf145d0be9
ms.date: 4/26/2023
ms.keywords: IWMProfile interface [windows Media Format],RemoveStream method, IWMProfile.RemoveStream, IWMProfile2 interface [windows Media Format],RemoveStream method, IWMProfile2::RemoveStream, IWMProfile3 interface [windows Media Format],RemoveStream method, IWMProfile3::RemoveStream, IWMProfile::RemoveStream, IWMProfileRemoveStream, RemoveStream, RemoveStream method [windows Media Format], RemoveStream method [windows Media Format],IWMProfile interface, RemoveStream method [windows Media Format],IWMProfile2 interface, RemoveStream method [windows Media Format],IWMProfile3 interface, wmformat.iwmprofile_removestream, wmsdkidl/IWMProfile2::RemoveStream, wmsdkidl/IWMProfile3::RemoveStream, wmsdkidl/IWMProfile::RemoveStream
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
 - IWMProfile::RemoveStream
 - wmsdkidl/IWMProfile::RemoveStream
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
 - qasf.dll
api_name:
 - IWMProfile.RemoveStream
 - IWMProfile2.RemoveStream
 - IWMProfile3.RemoveStream
---

# IWMProfile::RemoveStream


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>RemoveStream</b> method removes a stream from the profile.

## -parameters

### -param pConfig [in]

Pointer to the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig">IWMStreamConfig</a> interface of the stream configuration object that describes the stream you want to remove.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for an unspecified reason.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pConfig</i> parameter is <b>NULL</b> or not valid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/wmformat/iwmprofile">IWMProfile Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2">IWMProfile2</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-addstream">IWMProfile::AddStream</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-removestreambynumber">IWMProfile::RemoveStreamByNumber</a>