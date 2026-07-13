---
UID: NF:wmsdkidl.IWMLanguageList.GetLanguageDetails
title: IWMLanguageList::GetLanguageDetails (wmsdkidl.h)
description: The GetLanguageDetails method retrieves the RFC 1766-compliant language tag for an entry in the list of supported languages.
helpviewer_keywords: ["GetLanguageDetails","GetLanguageDetails method [windows Media Format]","GetLanguageDetails method [windows Media Format]","IWMLanguageList interface","IWMLanguageList interface [windows Media Format]","GetLanguageDetails method","IWMLanguageList.GetLanguageDetails","IWMLanguageList::GetLanguageDetails","IWMLanguageListGetLanguageDetails","wmformat.iwmlanguagelist_getlanguagedetails","wmsdkidl/IWMLanguageList::GetLanguageDetails"]
old-location: wmformat\iwmlanguagelist_getlanguagedetails.htm
tech.root: wmformat
ms.assetid: beb9f4fb-0acf-4693-b98e-2c197b330de5
ms.date: 4/26/2023
ms.keywords: GetLanguageDetails, GetLanguageDetails method [windows Media Format], GetLanguageDetails method [windows Media Format],IWMLanguageList interface, IWMLanguageList interface [windows Media Format],GetLanguageDetails method, IWMLanguageList.GetLanguageDetails, IWMLanguageList::GetLanguageDetails, IWMLanguageListGetLanguageDetails, wmformat.iwmlanguagelist_getlanguagedetails, wmsdkidl/IWMLanguageList::GetLanguageDetails
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
 - IWMLanguageList::GetLanguageDetails
 - wmsdkidl/IWMLanguageList::GetLanguageDetails
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
 - IWMLanguageList.GetLanguageDetails
---

# IWMLanguageList::GetLanguageDetails


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetLanguageDetails</b> method retrieves the RFC 1766-compliant language tag for an entry in the list of supported languages.

## -parameters

### -param wIndex [in]

<b>WORD</b> containing the index in the language list.

### -param pwszLanguageString [out]

Pointer to the RFC 1766-compliant language tag of the language list entry specified by <i>wIndex</i>. Pass <b>NULL</b> to retrieve the length of the string, which will be returned in <i>pcbLanguageStringLength</i>.

### -param pcchLanguageStringLength [in, out]

Pointer to a <b>WORD</b> containing the length of the language string, in wide characters. This length includes the terminating <b>null</b> character.

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

For a list of common RFC 1766-compliant language identifiers, see <a href="/windows/desktop/wmformat/language-strings">Language Strings</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist">IWMLanguageList Interface</a>