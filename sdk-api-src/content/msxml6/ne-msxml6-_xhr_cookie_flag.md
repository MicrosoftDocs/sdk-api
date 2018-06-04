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

# _XHR_COOKIE_FLAG enumeration


## -description


Defines a set of flags that you can assign to a cookie in the HTTP cookie jar by calling the <a href="https://msdn.microsoft.com/E150B7CA-A881-4CD5-896F-7E3B6770E105">SetCookie</a> method or query from the HTTP cookie jar by calling the <a href="https://msdn.microsoft.com/A2A9C54B-92A2-41EA-A741-797BA219BCDA">GetCookie</a> method.


## -enum-fields




### -field XHR_COOKIE_IS_SECURE

The cookie is secure. 

When this flag is set, the client is only to return the cookie in subsequent requests if those requests use HTTPS.


### -field XHR_COOKIE_IS_SESSION

The cookie is only usable in the current HTTP session and is not persisted or saved.


### -field XHR_COOKIE_THIRD_PARTY

The cookie being set is a third-party cookie.


### -field XHR_COOKIE_PROMPT_REQUIRED

A prompt to the user is required to accept the cookie from the server.


### -field XHR_COOKIE_EVALUATE_P3P

The cookie has a Platform-for-Privacy-Protection (P3P) header. 



### -field XHR_COOKIE_APPLY_P3P

A cookie with a Platform-for-Privacy-Protection (P3P) header has been applied.


### -field XHR_COOKIE_P3P_ENABLED

A cookie with a Platform-for-Privacy-Protection (P3P) header has been enabled.


### -field XHR_COOKIE_IS_RESTRICTED

The cookie being set is associated with an untrusted site. 


### -field XHR_COOKIE_IE6


### -field XHR_COOKIE_IS_LEGACY


### -field XHR_COOKIE_NON_SCRIPT

Does not allow a script or other active content to access this cookie. 


### -field XHR_COOKIE_HTTPONLY

Enables the retrieval of cookies that are marked as "HTTPOnly". 

Do not use this flag if you expose a scriptable interface, because this has security implications. If you expose a scriptable interface, you can become an attack vector for cross-site scripting attacks. It is imperative that you use this flag only if they can guarantee that you will never permit third-party code to set a cookie using this flag by way of an extensibility mechanism you provide. 



## -see-also




<a href="https://msdn.microsoft.com/A2A9C54B-92A2-41EA-A741-797BA219BCDA">GetCookie</a>



<a href="https://msdn.microsoft.com/E150B7CA-A881-4CD5-896F-7E3B6770E105">SetCookie</a>



<a href="https://msdn.microsoft.com/208829B0-DBCC-4C22-910D-D6826283F8A0">XHR_COOKIE</a>
 

 

