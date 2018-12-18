---
UID: NF:wmsdkidl.IWMReaderAdvanced4.GetLanguageCount
title: IWMReaderAdvanced4::GetLanguageCount
author: windows-sdk-content
description: The GetLanguageCount method retrieves the total number of languages supported by an output. Only outputs associated with streams mutually exclusive by language will have more than one supported language.
old-location: wmformat\iwmreaderadvanced4_getlanguagecount.htm
tech.root: wmformat
ms.assetid: c63084cb-f4cf-413b-a3f1-eb6b1400ac93
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetLanguageCount, GetLanguageCount method [windows Media Format], GetLanguageCount method [windows Media Format],IWMReaderAdvanced4 interface, IWMReaderAdvanced4 interface [windows Media Format],GetLanguageCount method, IWMReaderAdvanced4.GetLanguageCount, IWMReaderAdvanced4::GetLanguageCount, IWMReaderAdvanced4GetLanguageCount, wmformat.iwmreaderadvanced4_getlanguagecount, wmsdkidl/IWMReaderAdvanced4::GetLanguageCount
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
 - IWMReaderAdvanced4.GetLanguageCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



This method should not be confused with <a href="https://msdn.microsoft.com/en-us/library/Dd757216(v=VS.85).aspx">IWMLanguageList::GetLanguageCount</a>. This method retrieves supported languages for a specific output. The methods of the <a href="https://msdn.microsoft.com/en-us/library/Dd757214(v=VS.85).aspx">IWMLanguageList</a> interface manipulate a list of languages at the file level. An individual output might not support all of the languages in the language list.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd757450(v=VS.85).aspx">IWMReaderAdvanced4 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757454(v=VS.85).aspx">IWMReaderAdvanced4::GetLanguage</a>
 

 

