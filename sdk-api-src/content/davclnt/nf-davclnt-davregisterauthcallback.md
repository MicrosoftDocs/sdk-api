---
UID: NF:davclnt.DavRegisterAuthCallback
title: DavRegisterAuthCallback function (davclnt.h)
description: Registers an application-defined callback function that the WebDAV client can use to prompt the user for credentials.
helpviewer_keywords: ["DavRegisterAuthCallback","DavRegisterAuthCallback function [WebDAV]","davclnt/DavRegisterAuthCallback","webdav.davregisterauthcallback"]
old-location: webdav\davregisterauthcallback.htm
tech.root: WebDAV
ms.assetid: 7b381929-174f-4b7b-aa22-dc7a2c3e3b4d
ms.date: 12/05/2018
ms.keywords: DavRegisterAuthCallback, DavRegisterAuthCallback function [WebDAV], davclnt/DavRegisterAuthCallback, webdav.davregisterauthcallback
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DavRegisterAuthCallback
 - davclnt/DavRegisterAuthCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Davclnt.dll
api_name:
 - DavRegisterAuthCallback
---

# DavRegisterAuthCallback function


## -description

Registers an application-defined callback function that the WebDAV client can use to prompt the user for credentials.

## -parameters

### -param CallBack [in]

A pointer to a function of type <a href="/windows/desktop/api/davclnt/nc-davclnt-pfndavauthcallback">PFNDAVAUTHCALLBACK</a>.

### -param Version [in]

This parameter is reserved for future use.

## -returns

If the function succeeds, the return value is an opaque handle. Note that <b>OPAQUE_HANDLE</b> is defined to be a <b>DWORD</b> value.

## -remarks

The WebDAV client uses the callback function when it is unable to connect to a remote resource using default credentials.

To unregister the callback function, use the <a href="/windows/desktop/api/davclnt/nf-davclnt-davunregisterauthcallback">DavUnregisterAuthCallback</a> function, passing the returned opaque handle in the <i>hCallback</i>  parameter.

## -see-also

<a href="/windows/desktop/api/davclnt/nf-davclnt-davunregisterauthcallback">DavUnregisterAuthCallback</a>