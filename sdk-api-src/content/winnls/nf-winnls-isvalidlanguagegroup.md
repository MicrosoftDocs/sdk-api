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

# IsValidLanguageGroup function


## -description


Determines if a language group is installed or supported on the operating system. For more information, see <a href="https://msdn.microsoft.com/daf929b2-8ff9-4a17-b294-f2c0eaef5848">NLS Terminology</a>.


## -parameters




### -param LanguageGroup [in]

Identifier of language group to validate. This parameter can have one of the following values:

<ul>
<li>LGRPID_ARABIC</li>
<li>
LGRPID_ARMENIAN
</li>
<li>LGRPID_BALTIC</li>
<li>LGRPID_CENTRAL_EUROPE</li>
<li>
LGRPID_CYRILLIC</li>
<li>
LGRPID_GEORGIAN
</li>
<li>LGRPID_GREEK</li>
<li>
LGRPID_HEBREW</li>
<li>
LGRPID_INDIC</li>
<li>LGRPID_JAPANESE</li>
<li>
LGRPID_KOREAN
</li>
<li>LGRPID_SIMPLIFIED_CHINESE</li>
<li>
LGRPID_TRADITIONAL_CHINESE</li>
<li>
LGRPID_THAI</li>
<li>LGRPID_TURKIC</li>
<li>
LGRPID_TURKISH
</li>
<li>LGRPID_VIETNAMESE</li>
<li>LGRPID_WESTERN_EUROPE</li>
</ul>

### -param dwFlags [in]

Flag specifying the validity test to apply to the language group identifier. This parameter can be set to one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LGRPID_INSTALLED"></a><a id="lgrpid_installed"></a><dl>
<dt><b>LGRPID_INSTALLED</b></dt>
</dl>
</td>
<td width="60%">
Determine if language group identifier is both supported and installed.

</td>
</tr>
<tr>
<td width="40%"><a id="LGRPID_SUPPORTED"></a><a id="lgrpid_supported"></a><dl>
<dt><b>LGRPID_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Determine if language group identifier is supported.

</td>
</tr>
</table>
 


## -returns



Returns <b>TRUE</b> if the language group identifier passes the specified validity test, or <b>FALSE</b> otherwise.




## -remarks



If the LGRPID_INSTALLED flag is specified and this function returns <b>TRUE</b>, the language group identifier is both supported and installed on the operating system.

If the LGRPID_SUPPORTED flag is specified and this function returns <b>TRUE</b>, the language group identifier is supported in the release, but not necessarily installed on the operating system.




## -see-also




<a href="https://msdn.microsoft.com/5a85c6bd-0362-46ff-80be-a198b1259482">EnumLanguageGroupLocales</a>



<a href="https://msdn.microsoft.com/8cc2335e-b222-44d9-a966-4b6803639071">EnumSystemLanguageGroups</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

