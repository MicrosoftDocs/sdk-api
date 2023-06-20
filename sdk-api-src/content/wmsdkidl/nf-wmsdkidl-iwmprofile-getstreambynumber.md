---
UID: NF:wmsdkidl.IWMProfile.GetStreamByNumber
title: IWMProfile::GetStreamByNumber (wmsdkidl.h)
description: The GetStreamByNumber method retrieves a stream from the profile.
helpviewer_keywords: ["GetStreamByNumber","GetStreamByNumber method [windows Media Format]","GetStreamByNumber method [windows Media Format]","IWMProfile interface","GetStreamByNumber method [windows Media Format]","IWMProfile2 interface","GetStreamByNumber method [windows Media Format]","IWMProfile3 interface","IWMProfile interface [windows Media Format]","GetStreamByNumber method","IWMProfile.GetStreamByNumber","IWMProfile2 interface [windows Media Format]","GetStreamByNumber method","IWMProfile2::GetStreamByNumber","IWMProfile3 interface [windows Media Format]","GetStreamByNumber method","IWMProfile3::GetStreamByNumber","IWMProfile::GetStreamByNumber","IWMProfileGetStreamByNumber","wmformat.iwmprofile_getstreambynumber","wmsdkidl/IWMProfile2::GetStreamByNumber","wmsdkidl/IWMProfile3::GetStreamByNumber","wmsdkidl/IWMProfile::GetStreamByNumber"]
old-location: wmformat\iwmprofile_getstreambynumber.htm
tech.root: wmformat
ms.assetid: 507b1c55-1ecb-41dd-a6e5-298e1047a7ea
ms.date: 4/26/2023
ms.keywords: GetStreamByNumber, GetStreamByNumber method [windows Media Format], GetStreamByNumber method [windows Media Format],IWMProfile interface, GetStreamByNumber method [windows Media Format],IWMProfile2 interface, GetStreamByNumber method [windows Media Format],IWMProfile3 interface, IWMProfile interface [windows Media Format],GetStreamByNumber method, IWMProfile.GetStreamByNumber, IWMProfile2 interface [windows Media Format],GetStreamByNumber method, IWMProfile2::GetStreamByNumber, IWMProfile3 interface [windows Media Format],GetStreamByNumber method, IWMProfile3::GetStreamByNumber, IWMProfile::GetStreamByNumber, IWMProfileGetStreamByNumber, wmformat.iwmprofile_getstreambynumber, wmsdkidl/IWMProfile2::GetStreamByNumber, wmsdkidl/IWMProfile3::GetStreamByNumber, wmsdkidl/IWMProfile::GetStreamByNumber
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
 - IWMProfile::GetStreamByNumber
 - wmsdkidl/IWMProfile::GetStreamByNumber
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
 - IWMProfile.GetStreamByNumber
 - IWMProfile2.GetStreamByNumber
 - IWMProfile3.GetStreamByNumber
---

# IWMProfile::GetStreamByNumber


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetStreamByNumber</b> method retrieves a stream from the profile.

## -parameters

### -param wStreamNum [in]

<b>WORD</b> containing the stream number.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppConfig</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_NO_STREAM</b></dt>
</dl>
</td>
<td width="60%">
The <i>wStreamNum</i> parameter is not valid.

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
</table>

## -remarks

Stream numbers are in the range of 1 through 63.

## -see-also

<a href="/windows/desktop/wmformat/iwmprofile">IWMProfile Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2">IWMProfile2</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstream">IWMProfile::GetStream</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-removestreambynumber">IWMProfile::RemoveStreamByNumber</a>