---
UID: NF:wmsdkidl.IWMProfile.GetMutualExclusionCount
title: IWMProfile::GetMutualExclusionCount (wmsdkidl.h)
description: The GetMutualExclusionCount method retrieves the number of mutual exclusion objects in the profile.
helpviewer_keywords: ["GetMutualExclusionCount","GetMutualExclusionCount method [windows Media Format]","GetMutualExclusionCount method [windows Media Format]","IWMProfile interface","GetMutualExclusionCount method [windows Media Format]","IWMProfile2 interface","GetMutualExclusionCount method [windows Media Format]","IWMProfile3 interface","IWMProfile interface [windows Media Format]","GetMutualExclusionCount method","IWMProfile.GetMutualExclusionCount","IWMProfile2 interface [windows Media Format]","GetMutualExclusionCount method","IWMProfile2::GetMutualExclusionCount","IWMProfile3 interface [windows Media Format]","GetMutualExclusionCount method","IWMProfile3::GetMutualExclusionCount","IWMProfile::GetMutualExclusionCount","IWMProfileGetMutualExclusionCount","wmformat.iwmprofile_getmutualexclusioncount","wmsdkidl/IWMProfile2::GetMutualExclusionCount","wmsdkidl/IWMProfile3::GetMutualExclusionCount","wmsdkidl/IWMProfile::GetMutualExclusionCount"]
old-location: wmformat\iwmprofile_getmutualexclusioncount.htm
tech.root: wmformat
ms.assetid: c223f75b-87c6-49bd-a16a-14b4751d5f1b
ms.date: 4/26/2023
ms.keywords: GetMutualExclusionCount, GetMutualExclusionCount method [windows Media Format], GetMutualExclusionCount method [windows Media Format],IWMProfile interface, GetMutualExclusionCount method [windows Media Format],IWMProfile2 interface, GetMutualExclusionCount method [windows Media Format],IWMProfile3 interface, IWMProfile interface [windows Media Format],GetMutualExclusionCount method, IWMProfile.GetMutualExclusionCount, IWMProfile2 interface [windows Media Format],GetMutualExclusionCount method, IWMProfile2::GetMutualExclusionCount, IWMProfile3 interface [windows Media Format],GetMutualExclusionCount method, IWMProfile3::GetMutualExclusionCount, IWMProfile::GetMutualExclusionCount, IWMProfileGetMutualExclusionCount, wmformat.iwmprofile_getmutualexclusioncount, wmsdkidl/IWMProfile2::GetMutualExclusionCount, wmsdkidl/IWMProfile3::GetMutualExclusionCount, wmsdkidl/IWMProfile::GetMutualExclusionCount
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
 - IWMProfile::GetMutualExclusionCount
 - wmsdkidl/IWMProfile::GetMutualExclusionCount
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
 - IWMProfile.GetMutualExclusionCount
 - IWMProfile2.GetMutualExclusionCount
 - IWMProfile3.GetMutualExclusionCount
---

# IWMProfile::GetMutualExclusionCount


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetMutualExclusionCount</b> method retrieves the number of mutual exclusion objects in the profile.

## -parameters

### -param pcME [out]

Pointer to a count of mutual exclusions.

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
The <i>pcME</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/wmformat/iwmprofile">IWMProfile Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2">IWMProfile2</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion">IWMProfile::GetMutualExclusion</a>



<a href="/windows/desktop/wmformat/mutual-exclusion">Mutual Exclusion</a>