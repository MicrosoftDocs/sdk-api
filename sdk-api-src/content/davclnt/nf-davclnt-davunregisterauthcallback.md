---
UID: NF:davclnt.DavUnregisterAuthCallback
title: DavUnregisterAuthCallback function
author: windows-sdk-content
description: Unregisters a registered callback function that the WebDAV client uses to prompt the user for credentials.
old-location: webdav\davunregisterauthcallback.htm
tech.root: WebDAV
ms.assetid: 5277d9ce-22e6-49d5-9a9c-c02993605bdf
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DavUnregisterAuthCallback, DavUnregisterAuthCallback function [WebDAV], davclnt/DavUnregisterAuthCallback, webdav.davunregisterauthcallback
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Davclnt.lib
req.dll: Davclnt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Davclnt.dll
api_name:
 - DavUnregisterAuthCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DavUnregisterAuthCallback function


## -description


Unregisters a registered callback function that the WebDAV client uses to prompt the user for credentials.


## -parameters




### -param hCallback [in]

The opaque handle that was returned by the <a href="https://msdn.microsoft.com/7b381929-174f-4b7b-aa22-dc7a2c3e3b4d">DavRegisterAuthCallback</a> function.


## -returns



This function does not return a value.




## -remarks



To register the callback function, use the <a href="https://msdn.microsoft.com/7b381929-174f-4b7b-aa22-dc7a2c3e3b4d">DavRegisterAuthCallback</a> function.




## -see-also




<a href="https://msdn.microsoft.com/7b381929-174f-4b7b-aa22-dc7a2c3e3b4d">DavRegisterAuthCallback</a>
 

 

