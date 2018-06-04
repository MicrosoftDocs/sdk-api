---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

