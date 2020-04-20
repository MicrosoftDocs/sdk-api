---
UID: NF:wmsdkidl.IWMProfile.GetName
title: IWMProfile::GetName (wmsdkidl.h)
description: The GetName method retrieves the name of a profile.helpviewer_keywords: ["GetName","GetName method [windows Media Format]","GetName method [windows Media Format]","IWMProfile interface","GetName method [windows Media Format]","IWMProfile2 interface","GetName method [windows Media Format]","IWMProfile3 interface","IWMProfile interface [windows Media Format]","GetName method","IWMProfile.GetName","IWMProfile2 interface [windows Media Format]","GetName method","IWMProfile2::GetName","IWMProfile3 interface [windows Media Format]","GetName method","IWMProfile3::GetName","IWMProfile::GetName","IWMProfileGetName","wmformat.iwmprofile_getname","wmsdkidl/IWMProfile2::GetName","wmsdkidl/IWMProfile3::GetName","wmsdkidl/IWMProfile::GetName"]
old-location: wmformat\iwmprofile_getname.htm
tech.root: wmformat
ms.assetid: c5993e47-842d-4392-9b54-2bf6f09c377c
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [windows Media Format], GetName method [windows Media Format],IWMProfile interface, GetName method [windows Media Format],IWMProfile2 interface, GetName method [windows Media Format],IWMProfile3 interface, IWMProfile interface [windows Media Format],GetName method, IWMProfile.GetName, IWMProfile2 interface [windows Media Format],GetName method, IWMProfile2::GetName, IWMProfile3 interface [windows Media Format],GetName method, IWMProfile3::GetName, IWMProfile::GetName, IWMProfileGetName, wmformat.iwmprofile_getname, wmsdkidl/IWMProfile2::GetName, wmsdkidl/IWMProfile3::GetName, wmsdkidl/IWMProfile::GetName
f1_keywords:
- wmsdkidl/IWMProfile.GetName
dev_langs:
- c++
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
- IWMProfile.GetName
- IWMProfile2.GetName
- IWMProfile3.GetName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMProfile::GetName


## -description



The <b>GetName</b> method retrieves the name of a profile.




## -parameters




### -param pwszName [out]

Pointer to a wide-character <b>null</b>-terminated string containing the name. Pass <b>NULL</b> to retrieve the length of the name.


### -param pcchName [in, out]

On input, specifies the length of the <i>pwszName</i> buffer. On output, if the method succeeds, specifies a pointer to the length of the name, including the terminating <b>null</b> character.


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
The <i>pwszName</i> parameter is not large enough.

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



You should make two calls to <b>GetName</b>. On the first call, pass <b>NULL</b> as <i>pwszName</i>. On return, the value pointed to by <i>pcchName</i> is set to the number of wide characters, including the terminating <b>null</b> character, required to hold the profile name. Then you can allocate the required amount of memory for the string and pass a pointer to it as <i>pwszName</i> on the second call.

Profiles have names and descriptions that are used when displaying lists of profiles.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/iwmprofile">IWMProfile Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2">IWMProfile2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-setname">IWMProfile::SetName</a>
 

 

