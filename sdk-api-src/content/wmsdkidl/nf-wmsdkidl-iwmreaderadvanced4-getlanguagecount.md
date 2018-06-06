---
UID: NF:wmsdkidl.IWMReaderAdvanced4.GetLanguageCount
title: IWMReaderAdvanced4::GetLanguageCount
author: windows-sdk-content
description: The GetLanguageCount method retrieves the total number of languages supported by an output. Only outputs associated with streams mutually exclusive by language will have more than one supported language.
old-location: wmformat\iwmreaderadvanced4_getlanguagecount.htm
old-project: wmformat
ms.assetid: c63084cb-f4cf-413b-a3f1-eb6b1400ac93
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetLanguageCount, GetLanguageCount method [windows Media Format], GetLanguageCount method [windows Media Format],IWMReaderAdvanced4 interface, IWMReaderAdvanced4 interface [windows Media Format],GetLanguageCount method, IWMReaderAdvanced4.GetLanguageCount, IWMReaderAdvanced4::GetLanguageCount, IWMReaderAdvanced4GetLanguageCount, wmformat.iwmreaderadvanced4_getlanguagecount, wmsdkidl/IWMReaderAdvanced4::GetLanguageCount
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
 - IWMReaderAdvanced4.GetLanguageCount
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderAdvanced4::GetLanguageCount


## -description



The <b>GetLanguageCount</b> method retrieves the total number of languages supported by an output. Only outputs associated with streams mutually exclusive by language will have more than one supported language.




## -parameters




### -param dwOutputNum [in]

<b>DWORD</b> containing the output number.


### -param pwLanguageCount [out]

Pointer to a <b>WORD</b> containing the language count.


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



This method should not be confused with <a href="https://msdn.microsoft.com/81c2edae-a793-421b-9aa2-39e280c43aeb">IWMLanguageList::GetLanguageCount</a>. This method retrieves supported languages for a specific output. The methods of the <a href="https://msdn.microsoft.com/63ef282c-d1ab-4ce9-a56b-209407c7839b">IWMLanguageList</a> interface manipulate a list of languages at the file level. An individual output might not support all of the languages in the language list.




## -see-also




<a href="https://msdn.microsoft.com/56695c57-f6c5-4c57-b3d4-73d169b379fa">IWMReaderAdvanced4 Interface</a>



<a href="https://msdn.microsoft.com/2af443f5-941a-466a-8eef-d4742f8e1ae1">IWMReaderAdvanced4::GetLanguage</a>
 

 

