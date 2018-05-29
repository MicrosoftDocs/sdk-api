---
UID: NS:davclnt._DAV_CALLBACK_AUTH_BLOB
title: "_DAV_CALLBACK_AUTH_BLOB"
author: windows-sdk-content
description: Stores an authentication BLOB that was retrieved by the DavAuthCallback callback function.
old-location: webdav\dav_callback_auth_blob.htm
old-project: WebDAV
ms.assetid: 59976cb0-ed68-4db0-b8f8-cfe5e778916b
ms.author: windowssdkdev
ms.date: 03/22/2018
ms.keywords: "*PDAV_CALLBACK_AUTH_BLOB, DAV_CALLBACK_AUTH_BLOB, DAV_CALLBACK_AUTH_BLOB structure [WebDAV], PDAV_CALLBACK_AUTH_BLOB, PDAV_CALLBACK_AUTH_BLOB structure pointer [WebDAV], _DAV_CALLBACK_AUTH_BLOB, davclnt/DAV_CALLBACK_AUTH_BLOB, davclnt/PDAV_CALLBACK_AUTH_BLOB, webdav.dav_callback_auth_blob"
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
req.typenames: DAV_CALLBACK_AUTH_BLOB, *PDAV_CALLBACK_AUTH_BLOB
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Davclnt.h
api_name:
-	DAV_CALLBACK_AUTH_BLOB
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DAV_CALLBACK_AUTH_BLOB structure


## -description


Stores an authentication <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> that was retrieved by the <a href="https://msdn.microsoft.com/6ac191ac-e63f-431f-893b-92c69320db58">DavAuthCallback</a> callback function.


## -struct-fields




### -field pBuffer

A pointer to a buffer that receives the authentication <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a>.


### -field ulSize

The size, in bytes, of the buffer that the <b>pBuffer</b> member points to.


### -field ulType

The data type of the buffer that the <b>pBuffer</b> member points to.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
PCCERT_CONTEXT

</td>
</tr>
</table>
 


## -remarks



This structure is included as a member in the <a href="https://msdn.microsoft.com/5414d7b5-b506-4d0a-a4b8-89ab7878d674">DAV_CALLBACK_CRED</a> structure.

The <a href="https://msdn.microsoft.com/96bacda5-8f24-4119-b0ae-82ff8aff54b4">DavFreeCredCallback</a> callback function should free only the buffer that the <b>pBuffer</b> member points to, not the entire structure.




## -see-also




<a href="https://msdn.microsoft.com/47420a67-bf3f-40d9-bfc4-ac2cb2776a40">DAV_CALLBACK_AUTH_UNP</a>



<a href="https://msdn.microsoft.com/6ac191ac-e63f-431f-893b-92c69320db58">DavAuthCallback</a>
 

 

