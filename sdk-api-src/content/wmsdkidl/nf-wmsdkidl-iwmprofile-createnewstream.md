---
UID: NF:wmsdkidl.IWMProfile.CreateNewStream
title: IWMProfile::CreateNewStream (wmsdkidl.h)
description: The CreateNewStream method creates a stream configuration object. You can use a stream configuration object to define the characteristics of a media stream.
helpviewer_keywords: ["CreateNewStream","CreateNewStream method [windows Media Format]","CreateNewStream method [windows Media Format]","IWMProfile interface","CreateNewStream method [windows Media Format]","IWMProfile2 interface","CreateNewStream method [windows Media Format]","IWMProfile3 interface","IWMProfile interface [windows Media Format]","CreateNewStream method","IWMProfile.CreateNewStream","IWMProfile2 interface [windows Media Format]","CreateNewStream method","IWMProfile2::CreateNewStream","IWMProfile3 interface [windows Media Format]","CreateNewStream method","IWMProfile3::CreateNewStream","IWMProfile::CreateNewStream","IWMProfileCreateNewStream","wmformat.iwmprofile_createnewstream","wmsdkidl/IWMProfile2::CreateNewStream","wmsdkidl/IWMProfile3::CreateNewStream","wmsdkidl/IWMProfile::CreateNewStream"]
old-location: wmformat\iwmprofile_createnewstream.htm
tech.root: wmformat
ms.assetid: 4a1478ff-00fb-46e2-97a3-e00e9c1b819a
ms.date: 4/26/2023
ms.keywords: CreateNewStream, CreateNewStream method [windows Media Format], CreateNewStream method [windows Media Format],IWMProfile interface, CreateNewStream method [windows Media Format],IWMProfile2 interface, CreateNewStream method [windows Media Format],IWMProfile3 interface, IWMProfile interface [windows Media Format],CreateNewStream method, IWMProfile.CreateNewStream, IWMProfile2 interface [windows Media Format],CreateNewStream method, IWMProfile2::CreateNewStream, IWMProfile3 interface [windows Media Format],CreateNewStream method, IWMProfile3::CreateNewStream, IWMProfile::CreateNewStream, IWMProfileCreateNewStream, wmformat.iwmprofile_createnewstream, wmsdkidl/IWMProfile2::CreateNewStream, wmsdkidl/IWMProfile3::CreateNewStream, wmsdkidl/IWMProfile::CreateNewStream
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
 - IWMProfile::CreateNewStream
 - wmsdkidl/IWMProfile::CreateNewStream
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
 - IWMProfile.CreateNewStream
 - IWMProfile2.CreateNewStream
 - IWMProfile3.CreateNewStream
---

# IWMProfile::CreateNewStream


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>CreateNewStream</b> method creates a stream configuration object. You can use a stream configuration object to define the characteristics of a media stream.

## -parameters

### -param guidStreamType [in]

GUID object specifying the major media type for the stream to be created (for example, WMMEDIATYPE_Video). The supported major types are listed in <a href="/windows/desktop/wmformat/media-types">Media Types</a>.

### -param ppConfig [out]

Pointer to a pointer to the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig">IWMStreamConfig</a> interface of the created stream configuration object.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough available memory.

</td>
</tr>
</table>

## -remarks

It is not possible to have a stream configuration object other than as an element of a profile. After the stream has been configured, this object must be added to the profile by using the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-addstream">AddStream</a> method.

When <b>CreateNewStream</b> is called, a valid stream number is specified for the new stream. Stream numbers are in the range of 1 through 63.

## -see-also

<a href="/windows/desktop/wmformat/iwmprofile">IWMProfile Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2">IWMProfile2</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3</a>



<a href="/windows/desktop/wmformat/stream-configuration-object">Stream Configuration Object</a>