---
UID: NF:authz.AuthzUninstallSecurityEventSource
title: AuthzUninstallSecurityEventSource function
author: windows-sdk-content
description: Removes the specified source from the list of valid security event sources.
old-location: security\authzuninstallsecurityeventsource.htm
tech.root: secauthz
ms.assetid: 495157da-d4ed-42ff-bcb4-5c07ab9ec0e6
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: AuthzUninstallSecurityEventSource, AuthzUninstallSecurityEventSource function [Security], authz/AuthzUninstallSecurityEventSource, security.authzuninstallsecurityeventsource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: authz.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Authz.lib
req.dll: Authz.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Authz.dll
api_name:
 - AuthzUninstallSecurityEventSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
- apiref
: 
- 
: 
- AuthzUninstallSecurityEventSource
: 
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
 

 

