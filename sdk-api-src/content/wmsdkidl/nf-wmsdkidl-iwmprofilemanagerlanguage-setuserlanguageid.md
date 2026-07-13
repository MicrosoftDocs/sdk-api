---
UID: NF:wmsdkidl.IWMProfileManagerLanguage.SetUserLanguageID
title: IWMProfileManagerLanguage::SetUserLanguageID (wmsdkidl.h)
description: The SetUserLanguageID method sets the language of the system profiles that will be parsed by the profile manager object.
helpviewer_keywords: ["IWMProfileManagerLanguage interface [windows Media Format]","SetUserLanguageID method","IWMProfileManagerLanguage.SetUserLanguageID","IWMProfileManagerLanguage::SetUserLanguageID","IWMProfileManagerLanguageSetUserLanguageID","SetUserLanguageID","SetUserLanguageID method [windows Media Format]","SetUserLanguageID method [windows Media Format]","IWMProfileManagerLanguage interface","wmformat.iwmprofilemanagerlanguage_setuserlanguageid","wmsdkidl/IWMProfileManagerLanguage::SetUserLanguageID"]
old-location: wmformat\iwmprofilemanagerlanguage_setuserlanguageid.htm
tech.root: wmformat
ms.assetid: e2154057-ea76-43bb-92d9-b52f16eb6b1b
ms.date: 4/26/2023
ms.keywords: IWMProfileManagerLanguage interface [windows Media Format],SetUserLanguageID method, IWMProfileManagerLanguage.SetUserLanguageID, IWMProfileManagerLanguage::SetUserLanguageID, IWMProfileManagerLanguageSetUserLanguageID, SetUserLanguageID, SetUserLanguageID method [windows Media Format], SetUserLanguageID method [windows Media Format],IWMProfileManagerLanguage interface, wmformat.iwmprofilemanagerlanguage_setuserlanguageid, wmsdkidl/IWMProfileManagerLanguage::SetUserLanguageID
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
 - IWMProfileManagerLanguage::SetUserLanguageID
 - wmsdkidl/IWMProfileManagerLanguage::SetUserLanguageID
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
 - IWMProfileManagerLanguage.SetUserLanguageID
---

# IWMProfileManagerLanguage::SetUserLanguageID


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

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

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage">IWMProfileManagerLanguage Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofilemanagerlanguage-getuserlanguageid">IWMProfileManagerLanguage::GetUserLanguageID</a>



<a href="/windows/desktop/wmformat/localized-system-profiles">Localized System Profiles</a>



<a href="/windows/desktop/wmformat/working-with-localized-system-profiles">Working with Localized System Profiles</a>