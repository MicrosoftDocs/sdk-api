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
 

 

