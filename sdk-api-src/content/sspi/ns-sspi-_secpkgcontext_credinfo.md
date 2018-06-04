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

# _SecPkgContext_CredInfo structure


## -description


Specifies the type of credentials used to create a client context.


## -struct-fields




### -field CredClass

A value of the <a href="https://msdn.microsoft.com/2f5f9be2-e7b5-4d34-a2ad-89a99db78ad0">SECPKG_CRED_CLASS</a> enumeration that indicates the type of credentials.


### -field IsPromptingNeeded

A nonzero value indicates that the application must prompt the user for credentials. All other values indicate that the application does not need to prompt the user.


## -see-also




<a href="https://msdn.microsoft.com/720b37dd-a957-4da9-8b94-4642e515bc22">SpQueryContextAttributes</a>
 

 

