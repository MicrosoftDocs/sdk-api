---
UID: NF:davclnt.DavRegisterAuthCallback
title: DavRegisterAuthCallback function
author: windows-sdk-content
description: Registers an application-defined callback function that the WebDAV client can use to prompt the user for credentials.
old-location: webdav\davregisterauthcallback.htm
old-project: webdav
ms.assetid: 7b381929-174f-4b7b-aa22-dc7a2c3e3b4d
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: DavRegisterAuthCallback, DavRegisterAuthCallback function [WebDAV], davclnt/DavRegisterAuthCallback, webdav.davregisterauthcallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: AUTHNEXTSTEP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Davclnt.dll
api_name:
 - DavRegisterAuthCallback
product: Windows
targetos: Windows
req.lib: Davclnt.lib
req.dll: Davclnt.dll
req.irql: 
---

# DavRegisterAuthCallback function


## -description


Registers an application-defined callback function that the WebDAV client can use to prompt the user for credentials.


## -parameters




### -param CallBack [in]

A pointer to a function of type <a href="https://msdn.microsoft.com/6ac191ac-e63f-431f-893b-92c69320db58">PFNDAVAUTHCALLBACK</a>.


### -param Version [in]

This parameter is reserved for future use.


## -returns



If the function succeeds, the return value is an opaque handle. Note that <b>OPAQUE_HANDLE</b> is defined to be a <b>DWORD</b> value.




## -remarks



The WebDAV client uses the callback function when it is unable to connect to a remote resource using default credentials.

To unregister the callback function, use the <a href="https://msdn.microsoft.com/5277d9ce-22e6-49d5-9a9c-c02993605bdf">DavUnregisterAuthCallback</a> function, passing the returned opaque handle in the <i>hCallback</i>  parameter.




## -see-also




<a href="https://msdn.microsoft.com/5277d9ce-22e6-49d5-9a9c-c02993605bdf">DavUnregisterAuthCallback</a>
 

 

