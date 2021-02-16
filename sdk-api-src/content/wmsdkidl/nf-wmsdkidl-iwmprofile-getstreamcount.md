---
UID: NF:wmsdkidl.IWMProfile.GetStreamCount
title: IWMProfile::GetStreamCount (wmsdkidl.h)
description: The GetStreamCount method retrieves the number of streams in a profile.
helpviewer_keywords: ["GetStreamCount","GetStreamCount method [windows Media Format]","GetStreamCount method [windows Media Format]","IWMProfile interface","GetStreamCount method [windows Media Format]","IWMProfile2 interface","GetStreamCount method [windows Media Format]","IWMProfile3 interface","IWMProfile interface [windows Media Format]","GetStreamCount method","IWMProfile.GetStreamCount","IWMProfile2 interface [windows Media Format]","GetStreamCount method","IWMProfile2::GetStreamCount","IWMProfile3 interface [windows Media Format]","GetStreamCount method","IWMProfile3::GetStreamCount","IWMProfile::GetStreamCount","IWMProfileGetStreamCount","wmformat.iwmprofile_getstreamcount","wmsdkidl/IWMProfile2::GetStreamCount","wmsdkidl/IWMProfile3::GetStreamCount","wmsdkidl/IWMProfile::GetStreamCount"]
old-location: wmformat\iwmprofile_getstreamcount.htm
tech.root: wmformat
ms.assetid: 49534bc3-9115-422b-b448-b6f9c6ec1c47
ms.date: 12/05/2018
ms.keywords: GetStreamCount, GetStreamCount method [windows Media Format], GetStreamCount method [windows Media Format],IWMProfile interface, GetStreamCount method [windows Media Format],IWMProfile2 interface, GetStreamCount method [windows Media Format],IWMProfile3 interface, IWMProfile interface [windows Media Format],GetStreamCount method, IWMProfile.GetStreamCount, IWMProfile2 interface [windows Media Format],GetStreamCount method, IWMProfile2::GetStreamCount, IWMProfile3 interface [windows Media Format],GetStreamCount method, IWMProfile3::GetStreamCount, IWMProfile::GetStreamCount, IWMProfileGetStreamCount, wmformat.iwmprofile_getstreamcount, wmsdkidl/IWMProfile2::GetStreamCount, wmsdkidl/IWMProfile3::GetStreamCount, wmsdkidl/IWMProfile::GetStreamCount
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
 - IWMProfile::GetStreamCount
 - wmsdkidl/IWMProfile::GetStreamCount
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
 - IWMProfile.GetStreamCount
 - IWMProfile2.GetStreamCount
 - IWMProfile3.GetStreamCount
---

# IWMProfile::GetStreamCount


## -description

The <b>GetStreamCount</b> method retrieves the number of streams in a profile.

## -parameters

### -param pcStreams [out]

Pointer to a count of streams.

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
The <i>pcStreams</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/wmformat/iwmprofile">IWMProfile Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2">IWMProfile2</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3</a>