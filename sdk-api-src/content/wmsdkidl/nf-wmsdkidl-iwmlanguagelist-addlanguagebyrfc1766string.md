---
UID: NF:wmsdkidl.IWMLanguageList.AddLanguageByRFC1766String
title: IWMLanguageList::AddLanguageByRFC1766String (wmsdkidl.h)
description: The AddLanguageByRFC1766String method adds an entry to the list of supported languages for a file based upon a language tag compliant with RFC 1766.
helpviewer_keywords: ["AddLanguageByRFC1766String","AddLanguageByRFC1766String method [windows Media Format]","AddLanguageByRFC1766String method [windows Media Format]","IWMLanguageList interface","IWMLanguageList interface [windows Media Format]","AddLanguageByRFC1766String method","IWMLanguageList.AddLanguageByRFC1766String","IWMLanguageList::AddLanguageByRFC1766String","IWMLanguageListAddLanguageByRFC1766String","wmformat.iwmlanguagelist_addlanguagebyrfc1766string","wmsdkidl/IWMLanguageList::AddLanguageByRFC1766String"]
old-location: wmformat\iwmlanguagelist_addlanguagebyrfc1766string.htm
tech.root: wmformat
ms.assetid: 3aec575c-8e04-4252-8863-1a458e56dcef
ms.date: 4/26/2023
ms.keywords: AddLanguageByRFC1766String, AddLanguageByRFC1766String method [windows Media Format], AddLanguageByRFC1766String method [windows Media Format],IWMLanguageList interface, IWMLanguageList interface [windows Media Format],AddLanguageByRFC1766String method, IWMLanguageList.AddLanguageByRFC1766String, IWMLanguageList::AddLanguageByRFC1766String, IWMLanguageListAddLanguageByRFC1766String, wmformat.iwmlanguagelist_addlanguagebyrfc1766string, wmsdkidl/IWMLanguageList::AddLanguageByRFC1766String
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
 - IWMLanguageList::AddLanguageByRFC1766String
 - wmsdkidl/IWMLanguageList::AddLanguageByRFC1766String
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
 - IWMLanguageList.AddLanguageByRFC1766String
---

# IWMLanguageList::AddLanguageByRFC1766String


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AddLanguageByRFC1766String</b> method adds an entry to the list of supported languages for a file based upon a language tag compliant with RFC 1766.

## -parameters

### -param pwszLanguageString [in]

Pointer to a wide-character null-terminated string containing an RFC 1766-compliant language tag.

### -param pwIndex [out]

Pointer to a <b>WORD</b>. On output, this will be set to the index assigned to the added language entry.

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