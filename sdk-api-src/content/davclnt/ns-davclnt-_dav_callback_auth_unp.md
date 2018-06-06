---
UID: NS:davclnt._DAV_CALLBACK_AUTH_UNP
title: "_DAV_CALLBACK_AUTH_UNP"
author: windows-sdk-content
description: Stores user name and password information that was retrieved by the DavAuthCallback callback function.
old-location: webdav\dav_callback_auth_unp.htm
old-project: WebDAV
ms.assetid: 47420a67-bf3f-40d9-bfc4-ac2cb2776a40
ms.author: windowssdkdev
ms.date: 03/22/2018
ms.keywords: "*PDAV_CALLBACK_AUTH_UNP, DAV_CALLBACK_AUTH_UNP, DAV_CALLBACK_AUTH_UNP structure [WebDAV], PDAV_CALLBACK_AUTH_UNP, PDAV_CALLBACK_AUTH_UNP structure pointer [WebDAV], _DAV_CALLBACK_AUTH_UNP, davclnt/DAV_CALLBACK_AUTH_UNP, davclnt/PDAV_CALLBACK_AUTH_UNP, webdav.dav_callback_auth_unp"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: davclnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 with SP2 [desktop apps only]
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
req.typenames: DAV_CALLBACK_AUTH_UNP, *PDAV_CALLBACK_AUTH_UNP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Davclnt.h
api_name:
 - DAV_CALLBACK_AUTH_UNP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DAV_CALLBACK_AUTH_UNP structure


## -description


Stores user name and password information that was retrieved by the <a href="https://msdn.microsoft.com/6ac191ac-e63f-431f-893b-92c69320db58">DavAuthCallback</a> callback function.


## -struct-fields




### -field pszUserName

A pointer to a string that contains the user name. This string is allocated by the <a href="https://msdn.microsoft.com/6ac191ac-e63f-431f-893b-92c69320db58">DavAuthCallback</a> callback function.


### -field ulUserNameLength

The length, in WCHAR, of the user name, not including the terminating <b>NULL</b> character.


### -field pszPassword

A pointer to a string that contains the password. This string is allocated by <a href="https://msdn.microsoft.com/6ac191ac-e63f-431f-893b-92c69320db58">DavAuthCallback</a>.


### -field ulPasswordLength

The length, in WCHAR, of the password, not including the terminating <b>NULL</b> character.


## -remarks



This structure is included as a member in the <a href="https://msdn.microsoft.com/5414d7b5-b506-4d0a-a4b8-89ab7878d674">DAV_CALLBACK_CRED</a> structure.

The <a href="https://msdn.microsoft.com/96bacda5-8f24-4119-b0ae-82ff8aff54b4">DavFreeCredCallback</a> callback function should free only the buffer that the <b>pBuffer</b> member points to, not the entire structure.




## -see-also




<a href="https://msdn.microsoft.com/59976cb0-ed68-4db0-b8f8-cfe5e778916b">DAV_CALLBACK_AUTH_BLOB</a>



<a href="https://msdn.microsoft.com/6ac191ac-e63f-431f-893b-92c69320db58">DavAuthCallback</a>
 

 

