---
UID: NF:wmsdkidl.IWMProfile.GetStream
title: IWMProfile::GetStream (wmsdkidl.h)
description: The GetStream method retrieves a stream from the profile.
helpviewer_keywords: ["GetStream","GetStream method [windows Media Format]","GetStream method [windows Media Format]","IWMProfile interface","GetStream method [windows Media Format]","IWMProfile2 interface","GetStream method [windows Media Format]","IWMProfile3 interface","IWMProfile interface [windows Media Format]","GetStream method","IWMProfile.GetStream","IWMProfile2 interface [windows Media Format]","GetStream method","IWMProfile2::GetStream","IWMProfile3 interface [windows Media Format]","GetStream method","IWMProfile3::GetStream","IWMProfile::GetStream","IWMProfileGetStream","wmformat.iwmprofile_getstream","wmsdkidl/IWMProfile2::GetStream","wmsdkidl/IWMProfile3::GetStream","wmsdkidl/IWMProfile::GetStream"]
old-location: wmformat\iwmprofile_getstream.htm
tech.root: wmformat
ms.assetid: 067c3f03-a79a-4693-b963-7081f79c72d3
ms.date: 12/05/2018
ms.keywords: GetStream, GetStream method [windows Media Format], GetStream method [windows Media Format],IWMProfile interface, GetStream method [windows Media Format],IWMProfile2 interface, GetStream method [windows Media Format],IWMProfile3 interface, IWMProfile interface [windows Media Format],GetStream method, IWMProfile.GetStream, IWMProfile2 interface [windows Media Format],GetStream method, IWMProfile2::GetStream, IWMProfile3 interface [windows Media Format],GetStream method, IWMProfile3::GetStream, IWMProfile::GetStream, IWMProfileGetStream, wmformat.iwmprofile_getstream, wmsdkidl/IWMProfile2::GetStream, wmsdkidl/IWMProfile3::GetStream, wmsdkidl/IWMProfile::GetStream
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
 - IWMProfile::GetStream
 - wmsdkidl/IWMProfile::GetStream
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
 - IWMProfile.GetStream
 - IWMProfile2.GetStream
 - IWMProfile3.GetStream
---

# IWMProfile::GetStream


## -description

The <b>GetStream</b> method retrieves a stream from the profile.

## -parameters

### -param dwStreamIndex [in]

<b>DWORD</b> containing the stream index.

### -param ppConfig [out]

Pointer to a pointer to the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig">IWMStreamConfig</a> interface of the stream configuration object that describes the specified stream.

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
<dt><b>E_FAIL</b></dt>
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
The <i>ppConfig</i> or <i>dwStreamIndex</i> parameter is not valid.

</td>
</tr>
</table>

## -remarks

You can use this method in conjunction with <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreamcount">GetStreamCount</a> to step through all of the streams in the profile.

## -see-also

<a href="/windows/desktop/wmformat/iwmprofile">IWMProfile Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2">IWMProfile2</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber">IWMProfile::GetStreamByNumber</a>