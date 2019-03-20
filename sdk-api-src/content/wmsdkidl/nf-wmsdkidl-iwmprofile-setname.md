---
UID: NF:wmsdkidl.IWMProfile.SetName
title: IWMProfile::SetName (wmsdkidl.h)
author: windows-sdk-content
description: The SetName method specifies the name of a profile.
old-location: wmformat\iwmprofile_setname.htm
tech.root: wmformat
ms.assetid: b4b38ec1-8fd8-4bfe-8513-33132379f6da
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMProfile interface [windows Media Format],SetName method, IWMProfile.SetName, IWMProfile2 interface [windows Media Format],SetName method, IWMProfile2::SetName, IWMProfile3 interface [windows Media Format],SetName method, IWMProfile3::SetName, IWMProfile::SetName, IWMProfileSetName, SetName, SetName method [windows Media Format], SetName method [windows Media Format],IWMProfile interface, SetName method [windows Media Format],IWMProfile2 interface, SetName method [windows Media Format],IWMProfile3 interface, wmformat.iwmprofile_setname, wmsdkidl/IWMProfile2::SetName, wmsdkidl/IWMProfile3::SetName, wmsdkidl/IWMProfile::SetName
ms.topic: method
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
 - IWMProfile.SetName
 - IWMProfile2.SetName
 - IWMProfile3.SetName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757266(v=VS.85).aspx">IWMProfile2</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757268(v=VS.85).aspx">IWMProfile3</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757405(v=VS.85).aspx">IWMProfile::GetName</a>
 

 

