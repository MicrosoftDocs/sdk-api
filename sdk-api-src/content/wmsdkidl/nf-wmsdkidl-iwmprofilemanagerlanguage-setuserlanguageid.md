---
UID: NF:wmsdkidl.IWMProfileManagerLanguage.SetUserLanguageID
title: IWMProfileManagerLanguage::SetUserLanguageID (wmsdkidl.h)
description: The SetUserLanguageID method sets the language of the system profiles that will be parsed by the profile manager object.helpviewer_keywords: ["IWMProfileManagerLanguage interface [windows Media Format]","SetUserLanguageID method","IWMProfileManagerLanguage.SetUserLanguageID","IWMProfileManagerLanguage::SetUserLanguageID","IWMProfileManagerLanguageSetUserLanguageID","SetUserLanguageID","SetUserLanguageID method [windows Media Format]","SetUserLanguageID method [windows Media Format]","IWMProfileManagerLanguage interface","wmformat.iwmprofilemanagerlanguage_setuserlanguageid","wmsdkidl/IWMProfileManagerLanguage::SetUserLanguageID"]
old-location: wmformat\iwmprofilemanagerlanguage_setuserlanguageid.htm
tech.root: wmformat
ms.assetid: e2154057-ea76-43bb-92d9-b52f16eb6b1b
ms.date: 12/05/2018
ms.keywords: IWMProfileManagerLanguage interface [windows Media Format],SetUserLanguageID method, IWMProfileManagerLanguage.SetUserLanguageID, IWMProfileManagerLanguage::SetUserLanguageID, IWMProfileManagerLanguageSetUserLanguageID, SetUserLanguageID, SetUserLanguageID method [windows Media Format], SetUserLanguageID method [windows Media Format],IWMProfileManagerLanguage interface, wmformat.iwmprofilemanagerlanguage_setuserlanguageid, wmsdkidl/IWMProfileManagerLanguage::SetUserLanguageID
f1_keywords:
- wmsdkidl/IWMProfileManagerLanguage.SetUserLanguageID
dev_langs:
- c++
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
api_name:
- IWMProfileManagerLanguage.SetUserLanguageID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMProfileManagerLanguage::SetUserLanguageID


## -description



The <b>SetUserLanguageID</b> method sets the language of the system profiles that will be parsed by the profile manager object.




## -parameters




### -param wLangID [in]

<b>WORD</b> containing the language identifier (LANGID) of the language you want to use.


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
<dt><b>NS_E_NOMATCHING_ELEMENT</b></dt>
</dl>
</td>
<td width="60%">
The specified LANGID represents a locality not supported by a localized set of system profiles.

</td>
</tr>
</table>
 




## -remarks



English – United States (0x0409) is the default language. This method will also return NS_E_MOMATCHING_ELEMENT for all languages except US English if you have not moved the correct .prx file into the system root directory.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage">IWMProfileManagerLanguage Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofilemanagerlanguage-getuserlanguageid">IWMProfileManagerLanguage::GetUserLanguageID</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/localized-system-profiles">Localized System Profiles</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/working-with-localized-system-profiles">Working with Localized System Profiles</a>
 

 

