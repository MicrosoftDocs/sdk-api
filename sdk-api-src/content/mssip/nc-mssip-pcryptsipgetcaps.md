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

# pCryptSIPGetCaps callback function


## -description


The <b>pCryptSIPGetCaps</b> function is implemented by an <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">subject interface package</a> (SIP) to report capabilities.


## -parameters




### -param *pSubjInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/6274cd08-d67f-410d-9303-3a42b7f1edc6">SIP_SUBJECTINFO</a> structure that specifies subject information data to the SIP APIs.


### -param *pCaps [in, out]

Pointer to a <a href="https://msdn.microsoft.com/0B6D173B-0183-4A7C-BB92-2D451F746164">SIP_CAP_SET</a> structure that defines the capabilities of an SIP.


## -see-also




<a href="https://msdn.microsoft.com/F939F6D5-DDFE-478F-8FDD-8FA9FAB26010">CryptSIPGetCaps</a>



<a href="https://msdn.microsoft.com/0B6D173B-0183-4A7C-BB92-2D451F746164">SIP_CAP_SET</a>



<a href="https://msdn.microsoft.com/6274cd08-d67f-410d-9303-3a42b7f1edc6">SIP_SUBJECTINFO</a>
 

 

