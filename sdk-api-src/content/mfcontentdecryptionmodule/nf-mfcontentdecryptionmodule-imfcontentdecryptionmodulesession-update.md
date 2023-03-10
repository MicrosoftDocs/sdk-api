---
UID: NF:mfcontentdecryptionmodule.IMFContentDecryptionModuleSession.Update
title: IMFContentDecryptionModuleSession::Update
ms.date: 11/26/2019
targetos: Windows
description: Provides messages, including licenses, to the Content Decryption Module (CDM) session.
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
 - IMFContentDecryptionModuleSession::Update
f1_keywords:
 - IMFContentDecryptionModuleSession::Update
 - mfcontentdecryptionmodule/IMFContentDecryptionModuleSession::Update
dev_langs:
 - c++
---

## -description

Provides messages, including licenses, to the Content Decryption Module (CDM) session. Persisted data should not be released or cleared.

## -parameters

### -param response

A **BYTE** array containing messages.

### -param responseSize

The size of the **BYTE** array provided in the *response* parameter.

## -returns

Returns S_OK on success.

## -remarks

**Update** is based on the Encrypted Media Extension specification's [MediaKeySession.update](https://www.w3.org/TR/2017/REC-encrypted-media-20170918/#dom-mediakeysession-update).

## -see-also

