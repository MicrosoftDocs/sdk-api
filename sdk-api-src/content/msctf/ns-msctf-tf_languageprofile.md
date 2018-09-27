---
UID: NS:msctf.TF_LANGUAGEPROFILE
title: TF_LANGUAGEPROFILE
author: windows-sdk-content
description: The TF_LANGUAGEPROFILE structure contains information about a language profile.
old-location: tsf\tf_languageprofile.htm
tech.root: TSF
ms.assetid: f9dbd701-d893-409b-b033-3e37d12ccaa7
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: TF_LANGUAGEPROFILE, TF_LANGUAGEPROFILE structure [Text Services Framework], _tsf_tf_languageprofile_ref, msctf/TF_LANGUAGEPROFILE, tsf.tf_languageprofile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msctf.h
api_name:
 - TF_LANGUAGEPROFILE
product: Windows
targetos: Windows
req.typenames: TF_LANGUAGEPROFILE
req.redist: TSF 1.0 on Windows 2000 Professional
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
 

 

