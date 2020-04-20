---
UID: NF:wmsdkidl.IWMLanguageList.GetLanguageCount
title: IWMLanguageList::GetLanguageCount (wmsdkidl.h)
description: The GetLanguageCount method retrieves the total number of supported languages in the language list.helpviewer_keywords: ["GetLanguageCount","GetLanguageCount method [windows Media Format]","GetLanguageCount method [windows Media Format]","IWMLanguageList interface","IWMLanguageList interface [windows Media Format]","GetLanguageCount method","IWMLanguageList.GetLanguageCount","IWMLanguageList::GetLanguageCount","IWMLanguageListGetLanguageCount","wmformat.iwmlanguagelist_getlanguagecount","wmsdkidl/IWMLanguageList::GetLanguageCount"]
old-location: wmformat\iwmlanguagelist_getlanguagecount.htm
tech.root: wmformat
ms.assetid: 81c2edae-a793-421b-9aa2-39e280c43aeb
ms.date: 12/05/2018
ms.keywords: GetLanguageCount, GetLanguageCount method [windows Media Format], GetLanguageCount method [windows Media Format],IWMLanguageList interface, IWMLanguageList interface [windows Media Format],GetLanguageCount method, IWMLanguageList.GetLanguageCount, IWMLanguageList::GetLanguageCount, IWMLanguageListGetLanguageCount, wmformat.iwmlanguagelist_getlanguagecount, wmsdkidl/IWMLanguageList::GetLanguageCount
f1_keywords:
- wmsdkidl/IWMLanguageList.GetLanguageCount
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
- IWMLanguageList.GetLanguageCount
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMLanguageList::GetLanguageCount


## -description



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



For a list of common RFC 1766-compliant language identifiers, see <a href="https://docs.microsoft.com/windows/desktop/wmformat/language-strings">Language Strings</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist">IWMLanguageList Interface</a>
 

 

