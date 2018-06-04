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

# CryptSIPGetCaps function


## -description


The <b>CryptSIPGetCaps</b> function retrieves the capabilities of a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">subject interface package</a> (SIP).


## -parameters




### -param pSubjInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/6274cd08-d67f-410d-9303-3a42b7f1edc6">SIP_SUBJECTINFO</a> structure that specifies subject information data to the SIP APIs.


### -param pCaps [in, out]

Pointer to a <a href="https://msdn.microsoft.com/0B6D173B-0183-4A7C-BB92-2D451F746164">SIP_CAP_SET</a> structure that defines the capabilities of an SIP.


## -remarks



Unlike other SIP functions, <b>CryptSIPGetCaps</b> is not registered in the dispatch table. For more information, see the <a href="https://msdn.microsoft.com/d34b5081-0af8-4dcc-8133-a91d0603d419">SIP_DISPATCH_INFO</a> structure. Instead, callers must map the object identifier (OID) to the function entry point. 




## -see-also




<a href="https://msdn.microsoft.com/0B6D173B-0183-4A7C-BB92-2D451F746164">SIP_CAP_SET</a>



<a href="https://msdn.microsoft.com/6274cd08-d67f-410d-9303-3a42b7f1edc6">SIP_SUBJECTINFO</a>



<a href="https://msdn.microsoft.com/8EA46B67-F542-4B15-81F4-3DD83DD45764">pCryptSIPGetCaps</a>
 

 

