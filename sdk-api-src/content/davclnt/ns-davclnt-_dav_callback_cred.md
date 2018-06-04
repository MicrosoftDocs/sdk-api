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

# _DAV_CALLBACK_CRED structure


## -description


Stores user credential information  that was retrieved by the <a href="https://msdn.microsoft.com/6ac191ac-e63f-431f-893b-92c69320db58">DavAuthCallback</a> callback function.


## -struct-fields




### -field AuthBlob

If the <b>bAuthBlobValid</b> member is <b>TRUE</b>, this member is a <a href="https://msdn.microsoft.com/59976cb0-ed68-4db0-b8f8-cfe5e778916b">DAV_CALLBACK_AUTH_BLOB</a> structure that contains the user credential information.


### -field UNPBlob

If the <b>bAuthBlobValid</b> member is <b>FALSE</b>, this member is a <a href="https://msdn.microsoft.com/47420a67-bf3f-40d9-bfc4-ac2cb2776a40">DAV_CALLBACK_AUTH_UNP</a> structure that contains the user credential information.


### -field bAuthBlobValid

<b>TRUE</b> if the credential information is stored in the <b>AuthBlob</b> member, and the <b>UNPBlob</b> member should be ignored. <b>FALSE</b> if it is stored in the <b>UNPBlob</b> member, and the <b>AuthBlob</b> member should be ignored.


### -field bSave

<b>TRUE</b> if the credential information was written to the <a href="https://msdn.microsoft.com/a1105754-a57f-4a0d-9797-bec22b99900c">credential manager</a>, or <b>FALSE</b> otherwise.


## -remarks



This structure is used by the <a href="https://msdn.microsoft.com/6ac191ac-e63f-431f-893b-92c69320db58">DavAuthCallback</a> callback function.




## -see-also




<a href="https://msdn.microsoft.com/59976cb0-ed68-4db0-b8f8-cfe5e778916b">DAV_CALLBACK_AUTH_BLOB</a>



<a href="https://msdn.microsoft.com/47420a67-bf3f-40d9-bfc4-ac2cb2776a40">DAV_CALLBACK_AUTH_UNP</a>



<a href="https://msdn.microsoft.com/6ac191ac-e63f-431f-893b-92c69320db58">DavAuthCallback</a>



<a href="https://msdn.microsoft.com/96bacda5-8f24-4119-b0ae-82ff8aff54b4">DavFreeCredCallback</a>
 

 

