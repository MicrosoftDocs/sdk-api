---
UID: NE:mfidl.MF_MEDIAKEYSESSION_MESSAGETYPE
title: MF_MEDIAKEYSESSION_MESSAGETYPE
ms.date: 11/4/2019
targetos: Windows
description: Specifies the type of a Content Decryption Module (CDM) message.
tech.root: mf
req.construct-type: enumeration
req.ddi-compliance: 
req.header: mfidl.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MF_MEDIAKEYSESSION_MESSAGETYPE
f1_keywords:
 - MF_MEDIAKEYSESSION_MESSAGETYPE
 - mfidl/MF_MEDIAKEYSESSION_MESSAGETYPE
dev_langs:
 - c++
---

## -description

Specifies the type of a Content Decryption Module (CDM) message.

## -enum-fields

### -field MF_MEDIAKEYSESSION_MESSAGETYPE_LICENSE_REQUEST:0

The message contains a request for a new license.

### -field MF_MEDIAKEYSESSION_MESSAGETYPE_LICENSE_RENEWAL:1

The message contains a request to renew an existing license.

### -field MF_MEDIAKEYSESSION_MESSAGETYPE_LICENSE_RELEASE:2

The message contains a record of license destruction.

### -field MF_MEDIAKEYSESSION_MESSAGETYPE_INDIVIDUALIZATION_REQUEST:3

The message contains a request for App-Assisted Individualization (or re-individualization).

## -remarks

This value is used by the [IMFContentDecryptionModuleSessionCallbacks::KeyMessage](../mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmodulesessioncallbacks-keymessage.md) callback.

**MF_MEDIAKEYSESSION_MESSAGETYPE** is based on the Encrypted Media Extension specification's [MediaKeyStatus](https://www.w3.org/TR/2017/REC-encrypted-media-20170918/#dom-mediakeymessagetype) enumeration.

## -see-also

[IMFContentDecryptionModuleSessionCallbacks::KeyMessage](../mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmodulesessioncallbacks-keymessage.md)
