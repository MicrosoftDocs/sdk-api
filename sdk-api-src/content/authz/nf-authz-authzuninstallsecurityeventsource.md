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

# AuthzUninstallSecurityEventSource function


## -description


The <b>AuthzUninstallSecurityEventSource</b> function removes the specified source from the list of valid security event sources.


## -parameters




### -param dwFlags [in]

Reserved for future use; set this parameter to zero.


### -param szEventSourceName [in]

Name of the source to remove from the list of valid security event sources. This corresponds to  the <b>szEventSourceName</b> member of the <a href="https://msdn.microsoft.com/8b4d6e14-fb9c-428a-bd94-34eba668edc6">AUTHZ_SOURCE_SCHEMA_REGISTRATION</a> structure that defines the source.

This function removes the source information from the registry. For more information about the registry keys and values affected, see the <a href="https://msdn.microsoft.com/77cb5c6c-1634-4449-8d05-ce6357ad4e4b">AuthzInstallSecurityEventSource</a> function.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/8b4d6e14-fb9c-428a-bd94-34eba668edc6">AUTHZ_SOURCE_SCHEMA_REGISTRATION</a>



<a href="https://msdn.microsoft.com/77cb5c6c-1634-4449-8d05-ce6357ad4e4b">AuthzInstallSecurityEventSource</a>
 

 

