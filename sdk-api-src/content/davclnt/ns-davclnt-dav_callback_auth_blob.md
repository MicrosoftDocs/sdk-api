---
UID: NS:davclnt._DAV_CALLBACK_AUTH_BLOB
title: DAV_CALLBACK_AUTH_BLOB (davclnt.h)
description: Stores an authentication BLOB that was retrieved by the DavAuthCallback callback function.
helpviewer_keywords: ["*PDAV_CALLBACK_AUTH_BLOB","DAV_CALLBACK_AUTH_BLOB","DAV_CALLBACK_AUTH_BLOB structure [WebDAV]","PDAV_CALLBACK_AUTH_BLOB","PDAV_CALLBACK_AUTH_BLOB structure pointer [WebDAV]","davclnt/DAV_CALLBACK_AUTH_BLOB","davclnt/PDAV_CALLBACK_AUTH_BLOB","webdav.dav_callback_auth_blob"]
old-location: webdav\dav_callback_auth_blob.htm
tech.root: WebDAV
ms.assetid: 59976cb0-ed68-4db0-b8f8-cfe5e778916b
ms.date: 12/05/2018
ms.keywords: '*PDAV_CALLBACK_AUTH_BLOB, DAV_CALLBACK_AUTH_BLOB, DAV_CALLBACK_AUTH_BLOB structure [WebDAV], PDAV_CALLBACK_AUTH_BLOB, PDAV_CALLBACK_AUTH_BLOB structure pointer [WebDAV], davclnt/DAV_CALLBACK_AUTH_BLOB, davclnt/PDAV_CALLBACK_AUTH_BLOB, webdav.dav_callback_auth_blob'
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
req.typenames: DAV_CALLBACK_AUTH_BLOB, *PDAV_CALLBACK_AUTH_BLOB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DAV_CALLBACK_AUTH_BLOB
 - davclnt/_DAV_CALLBACK_AUTH_BLOB
 - PDAV_CALLBACK_AUTH_BLOB
 - davclnt/PDAV_CALLBACK_AUTH_BLOB
 - DAV_CALLBACK_AUTH_BLOB
 - davclnt/DAV_CALLBACK_AUTH_BLOB
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
 - DAV_CALLBACK_AUTH_BLOB
---

# DAV_CALLBACK_AUTH_BLOB structure


## -description

Stores an authentication <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> that was retrieved by the <a href="/windows/desktop/api/davclnt/nc-davclnt-pfndavauthcallback">DavAuthCallback</a> callback function.

## -struct-fields

### -field pBuffer

A pointer to a buffer that receives the authentication <a href="/windows/desktop/SecGloss/b-gly">BLOB</a>.

### -field ulSize

The size, in bytes, of the buffer that the <b>pBuffer</b> member points to.

### -field ulType

The data type of the buffer that the <b>pBuffer</b> member points to.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
PCCERT_CONTEXT

</td>
</tr>
</table>

## -remarks

This structure is included as a member in the <a href="/windows/desktop/api/davclnt/ns-davclnt-dav_callback_cred">DAV_CALLBACK_CRED</a> structure.

The <a href="/windows/desktop/api/davclnt/nc-davclnt-pfndavauthcallback_freecred">DavFreeCredCallback</a> callback function should free only the buffer that the <b>pBuffer</b> member points to, not the entire structure.

## -see-also

<a href="/windows/desktop/api/davclnt/ns-davclnt-dav_callback_auth_unp">DAV_CALLBACK_AUTH_UNP</a>



<a href="/windows/desktop/api/davclnt/nc-davclnt-pfndavauthcallback">DavAuthCallback</a>