---
UID: NF:davclnt.DavUnregisterAuthCallback
title: DavUnregisterAuthCallback function (davclnt.h)
author: windows-sdk-content
description: Unregisters a registered callback function that the WebDAV client uses to prompt the user for credentials.
old-location: webdav\davunregisterauthcallback.htm
tech.root: WebDAV
ms.assetid: 5277d9ce-22e6-49d5-9a9c-c02993605bdf
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DavUnregisterAuthCallback, DavUnregisterAuthCallback function [WebDAV], davclnt/DavUnregisterAuthCallback, webdav.davunregisterauthcallback
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
ms.custom: 19H1
---

# DavUnregisterAuthCallback function


## -description


Unregisters a registered callback function that the WebDAV client uses to prompt the user for credentials.


## -parameters




### -param hCallback [in]

The opaque handle that was returned by the <a href="https://docs.microsoft.com/windows/desktop/api/davclnt/nf-davclnt-davregisterauthcallback">DavRegisterAuthCallback</a> function.


## -returns



This function does not return a value.




## -remarks



To register the callback function, use the <a href="https://docs.microsoft.com/windows/desktop/api/davclnt/nf-davclnt-davregisterauthcallback">DavRegisterAuthCallback</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/davclnt/nf-davclnt-davregisterauthcallback">DavRegisterAuthCallback</a>
 

 

