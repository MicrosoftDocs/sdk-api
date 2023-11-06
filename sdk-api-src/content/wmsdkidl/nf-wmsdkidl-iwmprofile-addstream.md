---
UID: NF:wmsdkidl.IWMProfile.AddStream
title: IWMProfile::AddStream (wmsdkidl.h)
description: The AddStream method adds a stream to the profile by copying the stream configuration details into the profile.
helpviewer_keywords: ["AddStream","AddStream method [windows Media Format]","AddStream method [windows Media Format]","IWMProfile interface","AddStream method [windows Media Format]","IWMProfile2 interface","AddStream method [windows Media Format]","IWMProfile3 interface","IWMProfile interface [windows Media Format]","AddStream method","IWMProfile.AddStream","IWMProfile2 interface [windows Media Format]","AddStream method","IWMProfile2::AddStream","IWMProfile3 interface [windows Media Format]","AddStream method","IWMProfile3::AddStream","IWMProfile::AddStream","IWMProfileAddStream","wmformat.iwmprofile_addstream","wmsdkidl/IWMProfile2::AddStream","wmsdkidl/IWMProfile3::AddStream","wmsdkidl/IWMProfile::AddStream"]
old-location: wmformat\iwmprofile_addstream.htm
tech.root: wmformat
ms.assetid: 3024fd2b-c261-49bd-b9a7-c1f43b31645b
ms.date: 4/26/2023
ms.keywords: AddStream, AddStream method [windows Media Format], AddStream method [windows Media Format],IWMProfile interface, AddStream method [windows Media Format],IWMProfile2 interface, AddStream method [windows Media Format],IWMProfile3 interface, IWMProfile interface [windows Media Format],AddStream method, IWMProfile.AddStream, IWMProfile2 interface [windows Media Format],AddStream method, IWMProfile2::AddStream, IWMProfile3 interface [windows Media Format],AddStream method, IWMProfile3::AddStream, IWMProfile::AddStream, IWMProfileAddStream, wmformat.iwmprofile_addstream, wmsdkidl/IWMProfile2::AddStream, wmsdkidl/IWMProfile3::AddStream, wmsdkidl/IWMProfile::AddStream
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
 - IWMProfile::AddStream
 - wmsdkidl/IWMProfile::AddStream
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
 - IWMProfile.AddStream
 - IWMProfile2.AddStream
 - IWMProfile3.AddStream
---

# IWMProfile::AddStream


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AddStream</b> method adds a stream to the profile by copying the stream configuration details into the profile.



Use <b>AddStream</b> only to include a stream that is new to the profile. New streams can be created by calling <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream">IWMProfile::CreateNewStream</a>, but will not be added to the profile until <b>AddStream</b> is called.

If you edit an existing stream using <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstream">IWMProfile::GetStream</a> or <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber">IWMProfile::GetStreamByNumber</a>, you should not call <b>AddStream</b> to include the changes. To include changes made to an existing stream, call <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream">IWMProfile::ReconfigStream</a>.

## -parameters

### -param pConfig [in]

Pointer to the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig">IWMStreamConfig</a> interface of the stream configuration object to be added to the profile. The stream must be configured by using the methods of the <b>IWMStreamConfig</b> interface before this method is used to add the stream to the profile.

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
The <i>pConfig</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough available memory.

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
<dt><b>NS_E_INVALID_STREAM</b></dt>
</dl>
</td>
<td width="60%">
The stream is not valid, possibly because it does not have a valid stream number.

</td>
</tr>
</table>

## -remarks

When a stream is added, its configuration is copied into the profile. A maximum of 63 streams can exist in a profile.

## -see-also

<a href="/windows/desktop/wmformat/iwmprofile">IWMProfile Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2">IWMProfile2</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstream">IWMProfile::GetStream</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-removestream">IWMProfile::RemoveStream</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig">IWMStreamConfig Interface</a>