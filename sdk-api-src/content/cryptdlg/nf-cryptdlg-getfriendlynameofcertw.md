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

# GetFriendlyNameOfCertW function


## -description


<p class="CCE_Message">[The <b>GetFriendlyNameOfCert</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/300e6345-0be0-48c7-a3a3-174879cf0bbb">CertGetNameString</a> function with the CERT_NAME_FRIENDLY_DISPLAY_TYPE flag.]

The <b>GetFriendlyNameOfCert</b> function retrieves the display name for a certificate.
<div class="alert"><b>Note</b>  This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to CryptDlg.dll.</div><div> </div>

## -parameters




### -param pccert [in]

A pointer to the certificate context whose display name is being retrieved.


### -param pwch

TBD


### -param cwch

TBD




#### - cchBuffer [in]

Number of characters allocated for <i>pchBuffer</i>, including the terminating <b>NULL</b> character.


#### - pchBuffer [out]

A pointer to a character string that receives the display name for the certificate.


## -returns



The return value is the number of characters, including the terminating <b>NULL</b> character, in the returned display name.



