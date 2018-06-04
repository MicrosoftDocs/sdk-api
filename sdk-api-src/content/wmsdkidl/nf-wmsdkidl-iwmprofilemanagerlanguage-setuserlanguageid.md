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

# IWMProfileManagerLanguage::SetUserLanguageID


## -description



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




<a href="https://msdn.microsoft.com/54875162-65fe-4959-b567-38c17ba2894d">IWMProfileManagerLanguage Interface</a>



<a href="https://msdn.microsoft.com/92d18ac9-8f68-47c6-91d7-de7653df69a6">IWMProfileManagerLanguage::GetUserLanguageID</a>



<a href="https://msdn.microsoft.com/2c218ab4-ecdb-414c-aa42-b71a42e340e5">Localized System Profiles</a>



<a href="https://msdn.microsoft.com/d911baf6-0731-4f02-9001-d04464a03f56">Working with Localized System Profiles</a>
 

 

