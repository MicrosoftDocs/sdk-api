---
UID: NE:msxml6._XHR_AUTH
title: XHR_AUTH (msxml6.h)
description: Specifies whether to allow authentication to be used to connect to a proxy or to connect to the HTTP server.
helpviewer_keywords: ["XHR_AUTH","XHR_AUTH enumeration [XMLHttpRequest2]","XHR_AUTH_ALL","XHR_AUTH_NONE","XHR_AUTH_PROXY","ixhr2.xhr_auth","msxml6/XHR_AUTH","msxml6/XHR_AUTH_ALL","msxml6/XHR_AUTH_NONE","msxml6/XHR_AUTH_PROXY"]
old-location: ixhr2\xhr_auth.htm
tech.root: ixhr2
ms.assetid: 82cc5e27-c669-424d-887d-ba7f5a5c9f02
ms.date: 12/05/2018
ms.keywords: XHR_AUTH, XHR_AUTH enumeration [XMLHttpRequest2], XHR_AUTH_ALL, XHR_AUTH_NONE, XHR_AUTH_PROXY, ixhr2.xhr_auth, msxml6/XHR_AUTH, msxml6/XHR_AUTH_ALL, msxml6/XHR_AUTH_NONE, msxml6/XHR_AUTH_PROXY
req.header: msxml6.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.typenames: XHR_AUTH
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _XHR_AUTH
 - msxml6/_XHR_AUTH
 - XHR_AUTH
 - msxml6/XHR_AUTH
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msxml6.h
api_name:
 - XHR_AUTH
---

# XHR_AUTH enumeration


## -description

Specifies whether to allow authentication to be used to connect to a proxy or to connect to the HTTP server.

## -enum-fields

### -field XHR_AUTH_ALL:0

Allow authentication to both proxy and server.

### -field XHR_AUTH_NONE:0x1

Disable authentication to both the proxy and server.

### -field XHR_AUTH_PROXY:0x2

Enable authentication to the proxy and disable auth to the server.

## -see-also

<a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-setproperty">SetProperty</a>
