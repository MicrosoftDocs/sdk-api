---
UID: NF:wmsdkidl.IWMProfile.SetName
title: IWMProfile::SetName (wmsdkidl.h)
description: The SetName method specifies the name of a profile.
helpviewer_keywords: ["IWMProfile interface [windows Media Format]","SetName method","IWMProfile.SetName","IWMProfile2 interface [windows Media Format]","SetName method","IWMProfile2::SetName","IWMProfile3 interface [windows Media Format]","SetName method","IWMProfile3::SetName","IWMProfile::SetName","IWMProfileSetName","SetName","SetName method [windows Media Format]","SetName method [windows Media Format]","IWMProfile interface","SetName method [windows Media Format]","IWMProfile2 interface","SetName method [windows Media Format]","IWMProfile3 interface","wmformat.iwmprofile_setname","wmsdkidl/IWMProfile2::SetName","wmsdkidl/IWMProfile3::SetName","wmsdkidl/IWMProfile::SetName"]
old-location: wmformat\iwmprofile_setname.htm
tech.root: wmformat
ms.assetid: b4b38ec1-8fd8-4bfe-8513-33132379f6da
ms.date: 12/05/2018
ms.keywords: IWMProfile interface [windows Media Format],SetName method, IWMProfile.SetName, IWMProfile2 interface [windows Media Format],SetName method, IWMProfile2::SetName, IWMProfile3 interface [windows Media Format],SetName method, IWMProfile3::SetName, IWMProfile::SetName, IWMProfileSetName, SetName, SetName method [windows Media Format], SetName method [windows Media Format],IWMProfile interface, SetName method [windows Media Format],IWMProfile2 interface, SetName method [windows Media Format],IWMProfile3 interface, wmformat.iwmprofile_setname, wmsdkidl/IWMProfile2::SetName, wmsdkidl/IWMProfile3::SetName, wmsdkidl/IWMProfile::SetName
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
 - IWMProfile::SetName
 - wmsdkidl/IWMProfile::SetName
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
 - IWMProfile.SetName
 - IWMProfile2.SetName
 - IWMProfile3.SetName
---

# IWMProfile::SetName


## -description

The <b>SetName</b> method specifies the name of a profile.

## -parameters

### -param pwszName [in]

Pointer to a wide-character <b>null</b>-terminated string containing the name. Profile names are limited to 256 wide characters.

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
The <i>pwszName</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

Profiles have names and descriptions, for use when displaying lists of profiles.

## -see-also

<a href="/windows/desktop/wmformat/iwmprofile">IWMProfile Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2">IWMProfile2</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getname">IWMProfile::GetName</a>