---
UID: NS:davclnt._DAV_CALLBACK_AUTH_UNP
title: DAV_CALLBACK_AUTH_UNP (davclnt.h)
description: Stores user name and password information that was retrieved by the DavAuthCallback callback function.
helpviewer_keywords: ["*PDAV_CALLBACK_AUTH_UNP","DAV_CALLBACK_AUTH_UNP","DAV_CALLBACK_AUTH_UNP structure [WebDAV]","PDAV_CALLBACK_AUTH_UNP","PDAV_CALLBACK_AUTH_UNP structure pointer [WebDAV]","davclnt/DAV_CALLBACK_AUTH_UNP","davclnt/PDAV_CALLBACK_AUTH_UNP","webdav.dav_callback_auth_unp"]
old-location: webdav\dav_callback_auth_unp.htm
tech.root: WebDAV
ms.assetid: 47420a67-bf3f-40d9-bfc4-ac2cb2776a40
ms.date: 12/05/2018
ms.keywords: '*PDAV_CALLBACK_AUTH_UNP, DAV_CALLBACK_AUTH_UNP, DAV_CALLBACK_AUTH_UNP structure [WebDAV], PDAV_CALLBACK_AUTH_UNP, PDAV_CALLBACK_AUTH_UNP structure pointer [WebDAV], davclnt/DAV_CALLBACK_AUTH_UNP, davclnt/PDAV_CALLBACK_AUTH_UNP, webdav.dav_callback_auth_unp'
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
req.typenames: DAV_CALLBACK_AUTH_UNP, *PDAV_CALLBACK_AUTH_UNP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DAV_CALLBACK_AUTH_UNP
 - davclnt/_DAV_CALLBACK_AUTH_UNP
 - PDAV_CALLBACK_AUTH_UNP
 - davclnt/PDAV_CALLBACK_AUTH_UNP
 - DAV_CALLBACK_AUTH_UNP
 - davclnt/DAV_CALLBACK_AUTH_UNP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Davclnt.h
api_name:
 - DAV_CALLBACK_AUTH_UNP
---

# DAV_CALLBACK_AUTH_UNP structure


## -description

Stores user name and password information that was retrieved by the <a href="/windows/desktop/api/davclnt/nc-davclnt-pfndavauthcallback">DavAuthCallback</a> callback function.

## -struct-fields

### -field pszUserName

A pointer to a string that contains the user name. This string is allocated by the <a href="/windows/desktop/api/davclnt/nc-davclnt-pfndavauthcallback">DavAuthCallback</a> callback function.

### -field ulUserNameLength

The length, in WCHAR, of the user name, not including the terminating <b>NULL</b> character.

### -field pszPassword

A pointer to a string that contains the password. This string is allocated by <a href="/windows/desktop/api/davclnt/nc-davclnt-pfndavauthcallback">DavAuthCallback</a>.

### -field ulPasswordLength

The length, in WCHAR, of the password, not including the terminating <b>NULL</b> character.

## -remarks

This structure is included as a member in the <a href="/windows/desktop/api/davclnt/ns-davclnt-dav_callback_cred">DAV_CALLBACK_CRED</a> structure.

The <a href="/windows/desktop/api/davclnt/nc-davclnt-pfndavauthcallback_freecred">DavFreeCredCallback</a> callback function should free only the buffer that the <b>pBuffer</b> member points to, not the entire structure.

## -see-also

<a href="/windows/desktop/api/davclnt/ns-davclnt-dav_callback_auth_blob">DAV_CALLBACK_AUTH_BLOB</a>



<a href="/windows/desktop/api/davclnt/nc-davclnt-pfndavauthcallback">DavAuthCallback</a>