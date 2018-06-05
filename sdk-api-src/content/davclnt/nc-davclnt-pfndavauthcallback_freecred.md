---
UID: NC:davclnt.PFNDAVAUTHCALLBACK_FREECRED
title: PFNDAVAUTHCALLBACK_FREECRED
author: windows-sdk-content
description: The WebDAV client calls the application-defined DavFreeCredCallback callback function to free the credential information that was retrieved by the DavAuthCallback callback function.
old-location: webdav\freecredcallback.htm
old-project: WebDAV
ms.assetid: 96bacda5-8f24-4119-b0ae-82ff8aff54b4
ms.author: windowssdkdev
ms.date: 03/22/2018
ms.keywords: DavFreeCredCallback, DavFreeCredCallback callback function [WebDAV], PFNDAVAUTHCALLBACK_FREECRED, PFNDAVAUTHCALLBACK_FREECRED callback, davclnt/DavFreeCredCallback, webdav.freecredcallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
req.typenames: D3DX11_FFT_DESC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Davclnt.h
api_name:
-	DavFreeCredCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PFNDAVAUTHCALLBACK_FREECRED callback function


## -description


The WebDAV client calls the application-defined <i>DavFreeCredCallback</i> callback function to free the credential information that was retrieved by the <a href="https://msdn.microsoft.com/6ac191ac-e63f-431f-893b-92c69320db58">DavAuthCallback</a> callback function.

The <i>PFNDAVAUTHCALLBACK_FREECRED</i> type defines a pointer to this callback function. <i>DavFreeCredCallback</i> is a placeholder for the application-defined function name.


## -parameters




### -param pbuffer [in]

A pointer to the <a href="https://msdn.microsoft.com/47420a67-bf3f-40d9-bfc4-ac2cb2776a40">DAV_CALLBACK_AUTH_UNP</a> or <a href="https://msdn.microsoft.com/59976cb0-ed68-4db0-b8f8-cfe5e778916b">DAV_CALLBACK_AUTH_BLOB</a>  structure that was used in the <a href="https://msdn.microsoft.com/6ac191ac-e63f-431f-893b-92c69320db58">DavAuthCallback</a> callback function.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



The <i>DavFreeCredCallback</i> callback function must be registered by calling the <a href="https://msdn.microsoft.com/7b381929-174f-4b7b-aa22-dc7a2c3e3b4d">DavRegisterAuthCallback</a> function.

This callback function should free only the buffer that the <b>pBuffer</b> member of the <a href="https://msdn.microsoft.com/47420a67-bf3f-40d9-bfc4-ac2cb2776a40">DAV_CALLBACK_AUTH_UNP</a> or <a href="https://msdn.microsoft.com/59976cb0-ed68-4db0-b8f8-cfe5e778916b">DAV_CALLBACK_AUTH_BLOB</a> structure points to, not the entire structure.




## -see-also




<a href="https://msdn.microsoft.com/5414d7b5-b506-4d0a-a4b8-89ab7878d674">DAV_CALLBACK_CRED</a>



<a href="https://msdn.microsoft.com/6ac191ac-e63f-431f-893b-92c69320db58">DavAuthCallback</a>
 

 

