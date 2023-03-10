---
UID: NF:davclnt.DavUnregisterAuthCallback
title: DavUnregisterAuthCallback function (davclnt.h)
description: Unregisters a registered callback function that the WebDAV client uses to prompt the user for credentials.
helpviewer_keywords: ["DavUnregisterAuthCallback","DavUnregisterAuthCallback function [WebDAV]","davclnt/DavUnregisterAuthCallback","webdav.davunregisterauthcallback"]
old-location: webdav\davunregisterauthcallback.htm
tech.root: WebDAV
ms.assetid: 5277d9ce-22e6-49d5-9a9c-c02993605bdf
ms.date: 12/05/2018
ms.keywords: DavUnregisterAuthCallback, DavUnregisterAuthCallback function [WebDAV], davclnt/DavUnregisterAuthCallback, webdav.davunregisterauthcallback
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
 - DavUnregisterAuthCallback
 - davclnt/DavUnregisterAuthCallback
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
 - DavUnregisterAuthCallback
---

## -description

Unregisters a registered callback function that the WebDAV client uses to prompt the user for credentials.

## -parameters

### -param hCallback [in]

The opaque handle that was returned by the <a href="/windows/desktop/api/davclnt/nf-davclnt-davregisterauthcallback">DavRegisterAuthCallback</a> function.

## -remarks

To register the callback function, use the <a href="/windows/desktop/api/davclnt/nf-davclnt-davregisterauthcallback">DavRegisterAuthCallback</a> function.

## -see-also

<a href="/windows/desktop/api/davclnt/nf-davclnt-davregisterauthcallback">DavRegisterAuthCallback</a>