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

# IAccDictionary::GetLocalizedString


## -description


Clients call the <b>IAccDictionary::GetLocalizedString</b> method to get localized strings for all system properties and their values.
<div class="alert"><b>Note</b>  Active Accessibility Text Services is deprecated. Please see     
<a href="http://go.microsoft.com/fwlink/p/?linkid=131573">Microsoft Windows Text Services Framework</a>
for more information on advanced text input and natural language technologies.
		</div><div> </div>

## -parameters




### -param Term [in]

Type: <b>REFGUID</b>

A globally unique identifier (GUID) that represents a property.


### -param lcid [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LCID</a></b>

The locale of the string to be returned.


### -param pResult [out]

Type: <b>BSTR*</b>

A localized string that represents the term.


### -param plcid [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LCID</a>*</b>

The language of the returned string.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If successful, returns S_OK.




## -remarks



This method returns the names of a property in the language specified by <i>lcid</i>. If that language is not on the system, Microsoft Active Accessibility finds the best match and returns the string in that language. If the <i>Term</i> parameter is not found in the dictionary, the <i>pResult</i> will be <b>NULL</b>.



