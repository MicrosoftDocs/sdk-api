---
UID: NF:wmsdkidl.IWMLanguageList.GetLanguageCount
title: IWMLanguageList::GetLanguageCount
author: windows-sdk-content
description: The GetLanguageCount method retrieves the total number of supported languages in the language list.
old-location: wmformat\iwmlanguagelist_getlanguagecount.htm
old-project: wmformat
ms.assetid: 81c2edae-a793-421b-9aa2-39e280c43aeb
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetLanguageCount, GetLanguageCount method [windows Media Format], GetLanguageCount method [windows Media Format],IWMLanguageList interface, IWMLanguageList interface [windows Media Format],GetLanguageCount method, IWMLanguageList.GetLanguageCount, IWMLanguageList::GetLanguageCount, IWMLanguageListGetLanguageCount, wmformat.iwmlanguagelist_getlanguagecount, wmsdkidl/IWMLanguageList::GetLanguageCount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WM_AETYPE
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
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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



For a list of common RFC 1766-compliant language identifiers, see <a href="https://msdn.microsoft.com/625f7e95-0d21-4e16-8323-0f6301a04b30">Language Strings</a>.




## -see-also




<a href="https://msdn.microsoft.com/63ef282c-d1ab-4ce9-a56b-209407c7839b">IWMLanguageList Interface</a>
 

 

