---
UID: NF:wmsdkidl.IWMProfileManagerLanguage.GetUserLanguageID
title: IWMProfileManagerLanguage::GetUserLanguageID (wmsdkidl.h)
description: The GetUserLanguageID method retrieves the language identifier for the system profiles loaded by the profile manager object.
helpviewer_keywords: ["GetUserLanguageID","GetUserLanguageID method [windows Media Format]","GetUserLanguageID method [windows Media Format]","IWMProfileManagerLanguage interface","IWMProfileManagerLanguage interface [windows Media Format]","GetUserLanguageID method","IWMProfileManagerLanguage.GetUserLanguageID","IWMProfileManagerLanguage::GetUserLanguageID","IWMProfileManagerLanguageGetUserLanguageID","wmformat.iwmprofilemanagerlanguage_getuserlanguageid","wmsdkidl/IWMProfileManagerLanguage::GetUserLanguageID"]
old-location: wmformat\iwmprofilemanagerlanguage_getuserlanguageid.htm
tech.root: wmformat
ms.assetid: 92d18ac9-8f68-47c6-91d7-de7653df69a6
ms.date: 12/05/2018
ms.keywords: GetUserLanguageID, GetUserLanguageID method [windows Media Format], GetUserLanguageID method [windows Media Format],IWMProfileManagerLanguage interface, IWMProfileManagerLanguage interface [windows Media Format],GetUserLanguageID method, IWMProfileManagerLanguage.GetUserLanguageID, IWMProfileManagerLanguage::GetUserLanguageID, IWMProfileManagerLanguageGetUserLanguageID, wmformat.iwmprofilemanagerlanguage_getuserlanguageid, wmsdkidl/IWMProfileManagerLanguage::GetUserLanguageID
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMProfileManagerLanguage::GetUserLanguageID
 - wmsdkidl/IWMProfileManagerLanguage::GetUserLanguageID
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
api_name:
 - IWMProfileManagerLanguage.GetUserLanguageID
---

# IWMProfileManagerLanguage::GetUserLanguageID


## -description

The <b>GetUserLanguageID</b> method retrieves the language identifier for the system profiles loaded by the profile manager object.

## -parameters

### -param wLangID [out]

Pointer to a <b>WORD</b> that receives the language identifier (LANGID) of the language set in the profile manager.

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
</table>

## -remarks

The default language is U.S. English (0x409).

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage">IWMProfileManagerLanguage Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofilemanagerlanguage-setuserlanguageid">IWMProfileManagerLanguage::SetUserLanguageID</a>



<a href="/windows/desktop/wmformat/localized-system-profiles">Localized System Profiles</a>



<a href="/windows/desktop/wmformat/working-with-localized-system-profiles">Working with Localized System Profiles</a>