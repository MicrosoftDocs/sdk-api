---
UID: NF:davclnt.DavDeleteConnection
title: DavDeleteConnection function (davclnt.h)
description: Closes a connection that was created by using the DavAddConnection function.
helpviewer_keywords: ["DavDeleteConnection","DavDeleteConnection function [WebDAV]","davclnt/DavDeleteConnection","webdav.davdeleteconnection"]
old-location: webdav\davdeleteconnection.htm
tech.root: WebDAV
ms.assetid: 736b8a16-30db-410e-8295-97730297d04b
ms.date: 12/05/2018
ms.keywords: DavDeleteConnection, DavDeleteConnection function [WebDAV], davclnt/DavDeleteConnection, webdav.davdeleteconnection
req.header: davclnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DavDeleteConnection
 - davclnt/DavDeleteConnection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - netapi32.dll
 - DavHlpr.dll
 - Ext-MS-Win-Rdr-DavHlpr-L1-1-0.dll
api_name:
 - DavDeleteConnection
---

# DavDeleteConnection function


## -description

Closes a connection that was created by using the <a href="/windows/desktop/api/davclnt/nf-davclnt-davaddconnection">DavAddConnection</a> function.

## -parameters

### -param ConnectionHandle [in]

A handle to an open connection that was  created by using the  <a href="/windows/desktop/api/davclnt/nf-davclnt-davaddconnection">DavAddConnection</a> function.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore">CertCloseStore</a>