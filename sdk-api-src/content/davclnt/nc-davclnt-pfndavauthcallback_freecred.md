---
UID: NC:davclnt.PFNDAVAUTHCALLBACK_FREECRED
title: PFNDAVAUTHCALLBACK_FREECRED (davclnt.h)
description: The WebDAV client calls the application-defined DavFreeCredCallback callback function to free the credential information that was retrieved by the DavAuthCallback callback function.
helpviewer_keywords: ["DavFreeCredCallback","DavFreeCredCallback callback function [WebDAV]","PFNDAVAUTHCALLBACK_FREECRED","PFNDAVAUTHCALLBACK_FREECRED callback","davclnt/DavFreeCredCallback","webdav.freecredcallback"]
old-location: webdav\freecredcallback.htm
tech.root: WebDAV
ms.assetid: 96bacda5-8f24-4119-b0ae-82ff8aff54b4
ms.date: 12/05/2018
ms.keywords: DavFreeCredCallback, DavFreeCredCallback callback function [WebDAV], PFNDAVAUTHCALLBACK_FREECRED, PFNDAVAUTHCALLBACK_FREECRED callback, davclnt/DavFreeCredCallback, webdav.freecredcallback
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFNDAVAUTHCALLBACK_FREECRED
 - davclnt/PFNDAVAUTHCALLBACK_FREECRED
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Davclnt.h
api_name:
 - DavFreeCredCallback
---

# PFNDAVAUTHCALLBACK_FREECRED callback function


## -description

The WebDAV client calls the application-defined <i>DavFreeCredCallback</i> callback function to free the credential information that was retrieved by the <a href="/windows/desktop/api/davclnt/nc-davclnt-pfndavauthcallback">DavAuthCallback</a> callback function.

The <i>PFNDAVAUTHCALLBACK_FREECRED</i> type defines a pointer to this callback function. <i>DavFreeCredCallback</i> is a placeholder for the application-defined function name.

## -parameters

### -param pbuffer [in]

A pointer to the <a href="/windows/desktop/api/davclnt/ns-davclnt-dav_callback_auth_unp">DAV_CALLBACK_AUTH_UNP</a> or <a href="/windows/desktop/api/davclnt/ns-davclnt-dav_callback_auth_blob">DAV_CALLBACK_AUTH_BLOB</a>  structure that was used in the <a href="/windows/desktop/api/davclnt/nc-davclnt-pfndavauthcallback">DavAuthCallback</a> callback function.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

The <i>DavFreeCredCallback</i> callback function must be registered by calling the <a href="/windows/desktop/api/davclnt/nf-davclnt-davregisterauthcallback">DavRegisterAuthCallback</a> function.

This callback function should free only the buffer that the <b>pBuffer</b> member of the <a href="/windows/desktop/api/davclnt/ns-davclnt-dav_callback_auth_unp">DAV_CALLBACK_AUTH_UNP</a> or <a href="/windows/desktop/api/davclnt/ns-davclnt-dav_callback_auth_blob">DAV_CALLBACK_AUTH_BLOB</a> structure points to, not the entire structure.

## -see-also

<a href="/windows/desktop/api/davclnt/ns-davclnt-dav_callback_cred">DAV_CALLBACK_CRED</a>



<a href="/windows/desktop/api/davclnt/nc-davclnt-pfndavauthcallback">DavAuthCallback</a>