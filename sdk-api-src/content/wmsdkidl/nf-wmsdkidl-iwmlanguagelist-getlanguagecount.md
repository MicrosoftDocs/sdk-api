---
UID: NF:wmsdkidl.IWMLanguageList.GetLanguageCount
title: IWMLanguageList::GetLanguageCount (wmsdkidl.h)
description: The GetLanguageCount method retrieves the total number of supported languages in the language list.
helpviewer_keywords: ["GetLanguageCount","GetLanguageCount method [windows Media Format]","GetLanguageCount method [windows Media Format]","IWMLanguageList interface","IWMLanguageList interface [windows Media Format]","GetLanguageCount method","IWMLanguageList.GetLanguageCount","IWMLanguageList::GetLanguageCount","IWMLanguageListGetLanguageCount","wmformat.iwmlanguagelist_getlanguagecount","wmsdkidl/IWMLanguageList::GetLanguageCount"]
old-location: wmformat\iwmlanguagelist_getlanguagecount.htm
tech.root: wmformat
ms.assetid: 81c2edae-a793-421b-9aa2-39e280c43aeb
ms.date: 4/26/2023
ms.keywords: GetLanguageCount, GetLanguageCount method [windows Media Format], GetLanguageCount method [windows Media Format],IWMLanguageList interface, IWMLanguageList interface [windows Media Format],GetLanguageCount method, IWMLanguageList.GetLanguageCount, IWMLanguageList::GetLanguageCount, IWMLanguageListGetLanguageCount, wmformat.iwmlanguagelist_getlanguagecount, wmsdkidl/IWMLanguageList::GetLanguageCount
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
 - IWMLanguageList::GetLanguageCount
 - wmsdkidl/IWMLanguageList::GetLanguageCount
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
 - IWMLanguageList.GetLanguageCount
---

# IWMLanguageList::GetLanguageCount


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetLanguageCount</b> method retrieves the total number of supported languages in the language list.

## -parameters

### -param pwCount [out]

Pointer to a <b>WORD</b> containing the total number of languages present in the language list.

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