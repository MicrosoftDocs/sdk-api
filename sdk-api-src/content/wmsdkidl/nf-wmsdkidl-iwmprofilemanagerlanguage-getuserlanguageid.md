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

# IWMProfileManagerLanguage::GetUserLanguageID


## -description



The <b>GetUserLanguageID</b> method retrieves the language identifier for the system profiles loaded by the profile manager object.




## -parameters




### -param wLangID [out]

Pointer to a <b>WORD</b> that receives the language identifier (LANGID) of the language set in the profile manager.


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



The default language is U.S. English (0x409).




## -see-also




<a href="https://msdn.microsoft.com/54875162-65fe-4959-b567-38c17ba2894d">IWMProfileManagerLanguage Interface</a>



<a href="https://msdn.microsoft.com/e2154057-ea76-43bb-92d9-b52f16eb6b1b">IWMProfileManagerLanguage::SetUserLanguageID</a>



<a href="https://msdn.microsoft.com/2c218ab4-ecdb-414c-aa42-b71a42e340e5">Localized System Profiles</a>



<a href="https://msdn.microsoft.com/d911baf6-0731-4f02-9001-d04464a03f56">Working with Localized System Profiles</a>
 

 

