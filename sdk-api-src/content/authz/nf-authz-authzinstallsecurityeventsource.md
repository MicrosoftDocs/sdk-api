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

# AuthzInstallSecurityEventSource function


## -description


The <b>AuthzInstallSecurityEventSource</b> function installs  the specified source as a security event source.


## -parameters




### -param dwFlags [in]

This parameter is reserved for future use and must be set to zero.


### -param pRegistration [in]

A pointer to an <a href="https://msdn.microsoft.com/8b4d6e14-fb9c-428a-bd94-34eba668edc6">AUTHZ_SOURCE_SCHEMA_REGISTRATION</a> structure that contains information about the security event source to be added.

The members of the <a href="https://msdn.microsoft.com/8b4d6e14-fb9c-428a-bd94-34eba668edc6">AUTHZ_SOURCE_SCHEMA_REGISTRATION</a> structure are used as follows to install the security event source in the security log key:

<ul>
<li>The <b>szEventSourceName</b> member is added as a registry key under <pre xml:space="preserve"><b>HKEY_LOCAL_MACHINE</b>
   <b>SYSTEM</b>
      <b>CurrentControlSet</b>
         <b>Services</b>
            <b>EventLog</b>
               <b>Security</b></pre>
</li>
<li>The <b>szEventMessageFile</b> member is added as the data in a REG_SZ value named <b>EventMessageFile</b> under the event source key.</li>
<li>The <b>szEventAccessStringsFile</b> member is added as the data in a REG_SZ value named <b>ParameterMessageFile</b> under the event source key.</li>
<li>If the registry path does not exist, it is created.</li>
</ul>
<ul>
<li>If the <b>szEventSourceXmlSchemaFile</b> member is not <b>NULL</b>, it is added as the data in a REG_SZ value named <b>XmlSchemaFile</b> under the event source key. This value is not used.</li>
<li>The <b>szExecutableImagePath</b> member may be set to <b>NULL</b>.</li>
</ul>

## -returns



If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/8b4d6e14-fb9c-428a-bd94-34eba668edc6">AUTHZ_SOURCE_SCHEMA_REGISTRATION</a>



<a href="https://msdn.microsoft.com/495157da-d4ed-42ff-bcb4-5c07ab9ec0e6">AuthzUninstallSecurityEventSource</a>
 

 

