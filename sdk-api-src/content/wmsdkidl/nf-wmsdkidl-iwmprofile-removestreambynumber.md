---
UID: NF:wmsdkidl.IWMProfile.RemoveStreamByNumber
title: IWMProfile::RemoveStreamByNumber (wmsdkidl.h)
description: The RemoveStreamByNumber method removes a stream from the profile.
helpviewer_keywords: ["IWMProfile interface [windows Media Format]","RemoveStreamByNumber method","IWMProfile.RemoveStreamByNumber","IWMProfile2 interface [windows Media Format]","RemoveStreamByNumber method","IWMProfile2::RemoveStreamByNumber","IWMProfile3 interface [windows Media Format]","RemoveStreamByNumber method","IWMProfile3::RemoveStreamByNumber","IWMProfile::RemoveStreamByNumber","IWMProfileRemoveStreamByNumber","RemoveStreamByNumber","RemoveStreamByNumber method [windows Media Format]","RemoveStreamByNumber method [windows Media Format]","IWMProfile interface","RemoveStreamByNumber method [windows Media Format]","IWMProfile2 interface","RemoveStreamByNumber method [windows Media Format]","IWMProfile3 interface","wmformat.iwmprofile_removestreambynumber","wmsdkidl/IWMProfile2::RemoveStreamByNumber","wmsdkidl/IWMProfile3::RemoveStreamByNumber","wmsdkidl/IWMProfile::RemoveStreamByNumber"]
old-location: wmformat\iwmprofile_removestreambynumber.htm
tech.root: wmformat
ms.assetid: 72ecc794-d393-416e-bc21-5a7756e76d99
ms.date: 12/05/2018
ms.keywords: IWMProfile interface [windows Media Format],RemoveStreamByNumber method, IWMProfile.RemoveStreamByNumber, IWMProfile2 interface [windows Media Format],RemoveStreamByNumber method, IWMProfile2::RemoveStreamByNumber, IWMProfile3 interface [windows Media Format],RemoveStreamByNumber method, IWMProfile3::RemoveStreamByNumber, IWMProfile::RemoveStreamByNumber, IWMProfileRemoveStreamByNumber, RemoveStreamByNumber, RemoveStreamByNumber method [windows Media Format], RemoveStreamByNumber method [windows Media Format],IWMProfile interface, RemoveStreamByNumber method [windows Media Format],IWMProfile2 interface, RemoveStreamByNumber method [windows Media Format],IWMProfile3 interface, wmformat.iwmprofile_removestreambynumber, wmsdkidl/IWMProfile2::RemoveStreamByNumber, wmsdkidl/IWMProfile3::RemoveStreamByNumber, wmsdkidl/IWMProfile::RemoveStreamByNumber
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
 - IWMProfile::RemoveStreamByNumber
 - wmsdkidl/IWMProfile::RemoveStreamByNumber
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
 - IWMProfile.RemoveStreamByNumber
 - IWMProfile2.RemoveStreamByNumber
 - IWMProfile3.RemoveStreamByNumber
---

# IWMProfile::RemoveStreamByNumber


## -description

The <b>RemoveStreamByNumber</b> method removes a stream from the profile.

## -parameters

### -param wStreamNum [in]

<b>WORD</b> containing the stream number.

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
<dt><b>NS_E_NO_STREAM</b></dt>
</dl>
</td>
<td width="60%">
No stream was found to match <i>wStreamNum</i> value.

</td>
</tr>
</table>

## -remarks

A stream may be included in other objects within the profile, such as mutual exclusion objects. This method will remove all references to the specified stream from all objects within the profile.

Stream numbers are in the range of 1 through 63.

## -see-also

<a href="/windows/desktop/wmformat/iwmprofile">IWMProfile Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2">IWMProfile2</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber">IWMProfile::GetStreamByNumber</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-removestream">IWMProfile::RemoveStream</a>