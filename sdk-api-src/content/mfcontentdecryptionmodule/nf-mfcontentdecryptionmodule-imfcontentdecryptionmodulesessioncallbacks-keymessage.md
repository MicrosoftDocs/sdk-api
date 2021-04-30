---
UID: NF:mfcontentdecryptionmodule.IMFContentDecryptionModuleSessionCallbacks.KeyMessage
title: IMFContentDecryptionModuleSessionCallbacks::KeyMessage
ms.date: 11/26/2019
targetos: Windows
description: Called when the Content Decryption Module (CDM) has generated a message for the session.
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
 - IMFContentDecryptionModuleSessionCallbacks::KeyMessage
f1_keywords:
 - IMFContentDecryptionModuleSessionCallbacks::KeyMessage
 - mfcontentdecryptionmodule/IMFContentDecryptionModuleSessionCallbacks::KeyMessage
dev_langs:
 - c++
---

## -description

Called when the Content Decryption Module (CDM) has generated a message for the session.

## -parameters

### -param messageType

A value from the [MF_MEDIAKEYSESSION_MESSAGETYPE](../mfidl/ne-mfidl-mf_mediakeysession_messagetype.md) enumeration specifying the type of the message.

### -param message

A pointer to a **BYTE** array containing the message contents. Messages are Key System-specific.

### -param messageSize

The size of the array in the *message* parameter.

### -param destinationURL

A optional parameter containing the destination URL.

## -returns

Returns an HRESULT.

## -remarks

**KeyMessage** is based on the Encrypted Media Extension specification's [MediaKeyMessageEvent](https://www.w3.org/TR/2017/REC-encrypted-media-20170918/#dom-mediakeymessageevent).

## -see-also