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

# _HTTP_SERVICE_CONFIG_URLACL_PARAM structure


## -description


The 
<b>HTTP_SERVICE_CONFIG_URLACL_PARAM</b> structure is used to specify the permissions associated with a particular record in the URL namespace reservation store. It is a member of the 
<a href="https://msdn.microsoft.com/92fc3f65-0153-4075-a61b-48a63c8e0ffe">HTTP_SERVICE_CONFIG_URLACL_SET</a> structure.


## -struct-fields




### -field pStringSecurityDescriptor

A pointer to a 
<a href="https://msdn.microsoft.com/0a226629-084c-40c5-bdd4-ad7355c807cf">Security Descriptor Definition Language (SDDL) string</a> that contains the permissions associated with this URL namespace reservation record.


## -remarks



The security descriptor string pointed to by the <b>pStringSecurityDescriptor</b> member has the following elements:



An example of a security descriptor string is:

<pre class="syntax" xml:space="preserve"><code>D:(A;;GX;;;S-1-0-0)(A;;GA;;;S-1-5-11)
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/92fc3f65-0153-4075-a61b-48a63c8e0ffe">HTTP_SERVICE_CONFIG_URLACL_SET</a>



<a href="https://msdn.microsoft.com/0a226629-084c-40c5-bdd4-ad7355c807cf">Security Descriptor String Format</a>
 

 

