---
UID: NF:authz.AuthzReportSecurityEventFromParams
title: AuthzReportSecurityEventFromParams function
author: windows-sdk-content
description: Generates a security audit for a registered security event source by using the specified array of audit parameters.
old-location: security\authzreportsecurityeventfromparams.htm
old-project: secauthz
ms.assetid: ee5b598a-0a89-4b32-a9bc-e9c811573b08
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: AuthzReportSecurityEventFromParams, AuthzReportSecurityEventFromParams function [Security], authz/AuthzReportSecurityEventFromParams, security.authzreportsecurityeventfromparams
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: authz.h
req.include-header: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
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
tech.root: 
req.typenames: AUTHZ_CONTEXT_INFORMATION_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Authz.dll
api_name:
 - AuthzReportSecurityEventFromParams
product: Windows
targetos: Windows
req.lib: Authz.lib
req.dll: Authz.dll
req.irql: 
---

# AuthzReportSecurityEventFromParams function


## -description


The <b>AuthzReportSecurityEventFromParams</b> function generates a security audit for a registered security event source by using the specified array of audit parameters.


## -parameters




### -param dwFlags [in]

Reserved for future use.


### -param hEventProvider [in]

A handle to the registered security event source to use for the audit.


### -param dwAuditId [in]

The identifier of the audit.


### -param pUserSid [in, optional]

A pointer to the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) that will be listed as the source of the audit in the event log.


### -param pParams [in]

An array of audit parameters.


## -returns



If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/726e480d-1a34-4fd6-ac2d-876fa08f4eae">AuthzRegisterSecurityEventSource</a>



<a href="https://msdn.microsoft.com/95d561ef-3233-433a-a1e7-b914df1dd211">AuthzReportSecurityEvent</a>
 

 

