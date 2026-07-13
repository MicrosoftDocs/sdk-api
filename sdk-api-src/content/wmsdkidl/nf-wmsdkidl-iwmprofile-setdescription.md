---
UID: NF:wmsdkidl.IWMProfile.SetDescription
title: IWMProfile::SetDescription (wmsdkidl.h)
description: The SetDescription method specifies the description of a profile. The description is a string that contains an explanation of what the profile should be used for.
helpviewer_keywords: ["IWMProfile interface [windows Media Format]","SetDescription method","IWMProfile.SetDescription","IWMProfile2 interface [windows Media Format]","SetDescription method","IWMProfile2::SetDescription","IWMProfile3 interface [windows Media Format]","SetDescription method","IWMProfile3::SetDescription","IWMProfile::SetDescription","IWMProfileSetDescription","SetDescription","SetDescription method [windows Media Format]","SetDescription method [windows Media Format]","IWMProfile interface","SetDescription method [windows Media Format]","IWMProfile2 interface","SetDescription method [windows Media Format]","IWMProfile3 interface","wmformat.iwmprofile_setdescription","wmsdkidl/IWMProfile2::SetDescription","wmsdkidl/IWMProfile3::SetDescription","wmsdkidl/IWMProfile::SetDescription"]
old-location: wmformat\iwmprofile_setdescription.htm
tech.root: wmformat
ms.assetid: 79ff6ba8-b94b-4c06-a7a5-18b6a8ebc222
ms.date: 4/26/2023
ms.keywords: IWMProfile interface [windows Media Format],SetDescription method, IWMProfile.SetDescription, IWMProfile2 interface [windows Media Format],SetDescription method, IWMProfile2::SetDescription, IWMProfile3 interface [windows Media Format],SetDescription method, IWMProfile3::SetDescription, IWMProfile::SetDescription, IWMProfileSetDescription, SetDescription, SetDescription method [windows Media Format], SetDescription method [windows Media Format],IWMProfile interface, SetDescription method [windows Media Format],IWMProfile2 interface, SetDescription method [windows Media Format],IWMProfile3 interface, wmformat.iwmprofile_setdescription, wmsdkidl/IWMProfile2::SetDescription, wmsdkidl/IWMProfile3::SetDescription, wmsdkidl/IWMProfile::SetDescription
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
 - IWMProfile::SetDescription
 - wmsdkidl/IWMProfile::SetDescription
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
 - IWMProfile.SetDescription
 - IWMProfile2.SetDescription
 - IWMProfile3.SetDescription
---

# IWMProfile::SetDescription


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetDescription</b> method specifies the description of a profile. The description is a string that contains an explanation of what the profile should be used for.

## -parameters

### -param pwszDescription [in]

Pointer to a wide-character <b>null</b>-terminated string containing the description. Profile descriptions are limited to 1024 wide characters.

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
The <i>pwszDescription</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/wmformat/iwmprofile">IWMProfile Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2">IWMProfile2</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getdescription">IWMProfile::GetDescription</a>