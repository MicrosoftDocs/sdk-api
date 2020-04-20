---
UID: NF:wmsdkidl.IWMProfile.GetVersion
title: IWMProfile::GetVersion (wmsdkidl.h)
description: The GetVersion method retrieves the version number of the Windows Media Format SDK used to create the profile.helpviewer_keywords: ["GetVersion","GetVersion method [windows Media Format]","GetVersion method [windows Media Format]","IWMProfile interface","GetVersion method [windows Media Format]","IWMProfile2 interface","GetVersion method [windows Media Format]","IWMProfile3 interface","IWMProfile interface [windows Media Format]","GetVersion method","IWMProfile.GetVersion","IWMProfile2 interface [windows Media Format]","GetVersion method","IWMProfile2::GetVersion","IWMProfile3 interface [windows Media Format]","GetVersion method","IWMProfile3::GetVersion","IWMProfile::GetVersion","IWMProfileGetVersion","wmformat.iwmprofile_getversion","wmsdkidl/IWMProfile2::GetVersion","wmsdkidl/IWMProfile3::GetVersion","wmsdkidl/IWMProfile::GetVersion"]
old-location: wmformat\iwmprofile_getversion.htm
tech.root: wmformat
ms.assetid: 4f74378e-4b60-4b49-8107-26eebdfab02a
ms.date: 12/05/2018
ms.keywords: GetVersion, GetVersion method [windows Media Format], GetVersion method [windows Media Format],IWMProfile interface, GetVersion method [windows Media Format],IWMProfile2 interface, GetVersion method [windows Media Format],IWMProfile3 interface, IWMProfile interface [windows Media Format],GetVersion method, IWMProfile.GetVersion, IWMProfile2 interface [windows Media Format],GetVersion method, IWMProfile2::GetVersion, IWMProfile3 interface [windows Media Format],GetVersion method, IWMProfile3::GetVersion, IWMProfile::GetVersion, IWMProfileGetVersion, wmformat.iwmprofile_getversion, wmsdkidl/IWMProfile2::GetVersion, wmsdkidl/IWMProfile3::GetVersion, wmsdkidl/IWMProfile::GetVersion
f1_keywords:
- wmsdkidl/IWMProfile.GetVersion
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
- IWMProfile.GetVersion
- IWMProfile2.GetVersion
- IWMProfile3.GetVersion
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMProfile::GetVersion


## -description



The <b>GetVersion</b> method retrieves the version number of the Windows Media Format SDK used to create the profile.




## -parameters




### -param pdwVersion [out]

Pointer to a <b>DWORD</b> containing one member of the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_version">WMT_VERSION</a> enumeration type. This value specifies the version of the Windows Media Format SDK that was used to create the profile.


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
The <i>pdwVersion</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The version number indicates the version of the Windows Media codecs used to encode content in the file. You should always use the latest codecs unless you have a specific need for backward compatibility.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/iwmprofile">IWMProfile Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2">IWMProfile2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3</a>
 

 

