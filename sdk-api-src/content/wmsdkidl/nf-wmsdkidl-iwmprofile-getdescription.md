---
UID: NF:wmsdkidl.IWMProfile.GetDescription
title: IWMProfile::GetDescription (wmsdkidl.h)
description: The GetDescription method retrieves the profile description. The description is a string that contains an explanation of what the profile should be used for.
helpviewer_keywords: ["GetDescription","GetDescription method [windows Media Format]","GetDescription method [windows Media Format]","IWMProfile interface","GetDescription method [windows Media Format]","IWMProfile2 interface","GetDescription method [windows Media Format]","IWMProfile3 interface","IWMProfile interface [windows Media Format]","GetDescription method","IWMProfile.GetDescription","IWMProfile2 interface [windows Media Format]","GetDescription method","IWMProfile2::GetDescription","IWMProfile3 interface [windows Media Format]","GetDescription method","IWMProfile3::GetDescription","IWMProfile::GetDescription","IWMProfileGetDescription","wmformat.iwmprofile_getdescription","wmsdkidl/IWMProfile2::GetDescription","wmsdkidl/IWMProfile3::GetDescription","wmsdkidl/IWMProfile::GetDescription"]
old-location: wmformat\iwmprofile_getdescription.htm
tech.root: wmformat
ms.assetid: fa680ddb-091b-4461-8979-9330f8d59cea
ms.date: 4/26/2023
ms.keywords: GetDescription, GetDescription method [windows Media Format], GetDescription method [windows Media Format],IWMProfile interface, GetDescription method [windows Media Format],IWMProfile2 interface, GetDescription method [windows Media Format],IWMProfile3 interface, IWMProfile interface [windows Media Format],GetDescription method, IWMProfile.GetDescription, IWMProfile2 interface [windows Media Format],GetDescription method, IWMProfile2::GetDescription, IWMProfile3 interface [windows Media Format],GetDescription method, IWMProfile3::GetDescription, IWMProfile::GetDescription, IWMProfileGetDescription, wmformat.iwmprofile_getdescription, wmsdkidl/IWMProfile2::GetDescription, wmsdkidl/IWMProfile3::GetDescription, wmsdkidl/IWMProfile::GetDescription
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
 - IWMProfile::GetDescription
 - wmsdkidl/IWMProfile::GetDescription
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
 - IWMProfile.GetDescription
 - IWMProfile2.GetDescription
 - IWMProfile3.GetDescription
---

# IWMProfile::GetDescription


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetDescription</b> method retrieves the profile description. The description is a string that contains an explanation of what the profile should be used for.

## -parameters

### -param pwszDescription [out]

Pointer to a wide-character <b>null</b>-terminated string containing the description. Pass <b>NULL</b> to retrieve the required length for the description.

### -param pcchDescription [in, out]

On input, specifies the length of the <i>pwszDescription</i> string. On output, if the method succeeds, specifies a pointer to a count of the number of characters in the name, including the terminating <b>null</b> character.

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
The <i>pcchName</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ASF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by the <i>pwszDescription</i> parameter is not large enough.

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
</table>

## -remarks

You should make two calls to <b>GetDescription</b>. On the first call, pass <b>NULL</b> as <i>pwszDescription</i>. On return, the value pointed to by <i>pcchDescription</i> is set to the number of wide characters, including the terminating <b>null</b> character, required to hold the profile description. Then you can allocate the required amount of memory for the string and pass a pointer to it as <i>pwszDescription</i> on the second call.

## -see-also

<a href="/windows/desktop/wmformat/iwmprofile">IWMProfile Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2">IWMProfile2</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-setdescription">IWMProfile::SetDescription</a>