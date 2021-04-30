---
UID: NF:mfcontentdecryptionmodule.IMFContentDecryptionModuleSession.GetExpiration
title: IMFContentDecryptionModuleSession::GetExpiration
ms.date: 11/26/2019
targetos: Windows
description: Gets the expiration time for all keys in the CDM session.
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
 - IMFContentDecryptionModuleSession::GetExpiration
f1_keywords:
 - IMFContentDecryptionModuleSession::GetExpiration
 - mfcontentdecryptionmodule/IMFContentDecryptionModuleSession::GetExpiration
dev_langs:
 - c++
---

## -description

Gets the expiration time for all keys in the session as determined by the Content Decryption Module (CDM).

## -parameters

### -param expiration

Receives a pointer to an LPWSTR representing the session ID or NaN if no such time exists or if the license explicitly never expires.

## -returns

Returns S_OK.

## -remarks

**GetExpiration** is based on the Encrypted Media Extension specification's [MediaKeySession.expiration](https://www.w3.org/TR/2017/REC-encrypted-media-20170918/#dom-mediakeysession-expiration). The time and time range values of the expiration are based on ECMA Language Specification's [Time Values and Time Range](https://tc39.es/ecma262/#sec-time-values-and-time-range).

## -see-also

