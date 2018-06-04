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

# TF_LANGUAGEPROFILE structure


## -description



The <b>TF_LANGUAGEPROFILE</b> structure contains information about a language profile.




## -struct-fields




### -field clsid

Specifies the class identifier of the text service within the language profile.


### -field langid

Specifies the language identifier of the profile.


### -field catid

Specifies the identifier of the category that the text service belongs to.


### -field fActive

A Boolean value, when <b>TRUE</b>, indicates that the language is activated.


### -field guidProfile

Specifies the identifier of the language profile.


## -see-also




<a href="https://msdn.microsoft.com/790fb0f4-4abd-4947-8e9a-68739657a8f8">IEnumTfLanguageProfiles::Next
      </a>
 

 

