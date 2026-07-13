---
UID: NF:wmsdkidl.IWMProfile.RemoveMutualExclusion
title: IWMProfile::RemoveMutualExclusion (wmsdkidl.h)
description: The RemoveMutualExclusion method removes a mutual exclusion object from the profile.
helpviewer_keywords: ["IWMProfile interface [windows Media Format]","RemoveMutualExclusion method","IWMProfile.RemoveMutualExclusion","IWMProfile2 interface [windows Media Format]","RemoveMutualExclusion method","IWMProfile2::RemoveMutualExclusion","IWMProfile3 interface [windows Media Format]","RemoveMutualExclusion method","IWMProfile3::RemoveMutualExclusion","IWMProfile::RemoveMutualExclusion","IWMProfileRemoveMutualExclusion","RemoveMutualExclusion","RemoveMutualExclusion method [windows Media Format]","RemoveMutualExclusion method [windows Media Format]","IWMProfile interface","RemoveMutualExclusion method [windows Media Format]","IWMProfile2 interface","RemoveMutualExclusion method [windows Media Format]","IWMProfile3 interface","wmformat.iwmprofile_removemutualexclusion","wmsdkidl/IWMProfile2::RemoveMutualExclusion","wmsdkidl/IWMProfile3::RemoveMutualExclusion","wmsdkidl/IWMProfile::RemoveMutualExclusion"]
old-location: wmformat\iwmprofile_removemutualexclusion.htm
tech.root: wmformat
ms.assetid: eb453285-a4e5-48dd-a4d0-72d2e09badc2
ms.date: 4/26/2023
ms.keywords: IWMProfile interface [windows Media Format],RemoveMutualExclusion method, IWMProfile.RemoveMutualExclusion, IWMProfile2 interface [windows Media Format],RemoveMutualExclusion method, IWMProfile2::RemoveMutualExclusion, IWMProfile3 interface [windows Media Format],RemoveMutualExclusion method, IWMProfile3::RemoveMutualExclusion, IWMProfile::RemoveMutualExclusion, IWMProfileRemoveMutualExclusion, RemoveMutualExclusion, RemoveMutualExclusion method [windows Media Format], RemoveMutualExclusion method [windows Media Format],IWMProfile interface, RemoveMutualExclusion method [windows Media Format],IWMProfile2 interface, RemoveMutualExclusion method [windows Media Format],IWMProfile3 interface, wmformat.iwmprofile_removemutualexclusion, wmsdkidl/IWMProfile2::RemoveMutualExclusion, wmsdkidl/IWMProfile3::RemoveMutualExclusion, wmsdkidl/IWMProfile::RemoveMutualExclusion
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
 - IWMProfile::RemoveMutualExclusion
 - wmsdkidl/IWMProfile::RemoveMutualExclusion
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
 - IWMProfile.RemoveMutualExclusion
 - IWMProfile2.RemoveMutualExclusion
 - IWMProfile3.RemoveMutualExclusion
---

# IWMProfile::RemoveMutualExclusion


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>RemoveMutualExclusion</b> method removes a mutual exclusion object from the profile.

## -parameters

### -param pME [in]

Pointer to the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion">IWMMutualExclusion</a> interface of the mutual exclusion object you want to remove.

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



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion">IWMProfile::AddMutualExclusion</a>