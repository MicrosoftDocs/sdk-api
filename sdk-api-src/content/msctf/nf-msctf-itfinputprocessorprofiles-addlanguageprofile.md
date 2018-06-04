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

# ITfInputProcessorProfiles::AddLanguageProfile


## -description




## -parameters




### -param rclsid [in]

Contains the text service CLSID.


### -param langid [in]

Contains a <b>LANGID</b> value that specifies the language identifier of the profile that the text service is added to. If this contains -1, the text service is added to all languages.


### -param guidProfile [in]

Contains a GUID value that identifies the language profile. This is the value obtained by <a href="https://msdn.microsoft.com/446bfda3-63d9-4070-b758-bdaf267c9911">ITfInputProcessorProfiles::GetActiveLanguageProfile</a> when the profile is active.


### -param pchDesc [in]

Pointer to a <b>WCHAR</b> buffer that contains the description string for the text service in the profile. This is the text service name displayed in the language bar.


### -param cchDesc [in]

Contains the length, in characters, of the description string in <i>pchDesc</i>. If this contains -1, <i>pchDesc</i> is assumed to be a <b>NULL</b>-terminated string.


### -param pchIconFile [in]

Pointer to a <b>WCHAR</b> buffer that contains the path and file name of the file that contains the icon to be displayed in the language bar for the text service in the profile. This file can be an executable (.exe), DLL (.dll) or icon (.ico) file.

This parameter is optional and can be <b>NULL</b>. In this case, a default icon is displayed for the text service.


### -param cchFile [in]

Contains the length, in characters, of the icon file string in <i>pchIconFile</i>. If this contains -1, <i>pchIconFile</i> is assumed to be a <b>NULL</b>-terminated string. This parameter is ignored if <i>pchIconFile</i> is <b>NULL</b>.


### -param uIconIndex [in]

Contains the zero-based index of the icon in <i>pchIconFile</i> to be displayed in the language bar for the text service in the profile. This parameter is ignored if <i>pchIconFile</i> is <b>NULL</b>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pszDesc</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9fa722a4-1e3f-4845-aea7-3b24b517f2a5">ITfInputProcessorProfiles</a>



<a href="https://msdn.microsoft.com/446bfda3-63d9-4070-b758-bdaf267c9911">ITfInputProcessorProfiles::GetActiveLanguageProfile
      </a>
 

 

