---
UID: NS:davclnt._DAV_CALLBACK_CRED
title: DAV_CALLBACK_CRED
author: windows-sdk-content
description: Stores user credential information that was retrieved by the DavAuthCallback callback function.
old-location: webdav\dav_callback_cred.htm
tech.root: WebDAV
ms.assetid: 5414d7b5-b506-4d0a-a4b8-89ab7878d674
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PDAV_CALLBACK_CRED, DAV_CALLBACK_CRED, DAV_CALLBACK_CRED structure [WebDAV], PDAV_CALLBACK_CRED, PDAV_CALLBACK_CRED structure pointer [WebDAV], davclnt/DAV_CALLBACK_CRED, davclnt/PDAV_CALLBACK_CRED, webdav.dav_callback_cred"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Davclnt.h
api_name:
 - DAV_CALLBACK_CRED
product: Windows
targetos: Windows
req.typenames: DAV_CALLBACK_CRED, *PDAV_CALLBACK_CRED
req.redist: 
---

# DAV_CALLBACK_CRED structure


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
 

 

