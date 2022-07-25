---
UID: NF:mfcontentdecryptionmodule.IMFContentDecryptionModuleSession.Close
title: IMFContentDecryptionModuleSession::Close
ms.date: 11/26/2019
targetos: Windows
description: Indicates that the application no longer needs the session and the Content Decryption Module (CDM) should release any resources associated with the session and close it.
tech.root: mf
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: mfcontentdecryptionmodule.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - mfcontentdecryptionmodule.h
api_name:
 - IMFContentDecryptionModuleSession::Close
f1_keywords:
 - IMFContentDecryptionModuleSession::Close
 - mfcontentdecryptionmodule/IMFContentDecryptionModuleSession::Close
dev_langs:
 - c++
---

## -description

Indicates that the application no longer needs the session and the Content Decryption Module (CDM) should release any resources associated with the session and close it.



## -returns

Returns S_OK on success.

## -remarks

**Close** is based on the Encrypted Media Extension specification's [MediaKeySession.close](https://www.w3.org/TR/2017/REC-encrypted-media-20170918/#dom-mediakeysession-close).

## -see-also

