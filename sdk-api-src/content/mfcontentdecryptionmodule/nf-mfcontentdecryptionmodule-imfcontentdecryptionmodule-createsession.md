---
UID: NF:mfcontentdecryptionmodule.IMFContentDecryptionModule.CreateSession
title: IMFContentDecryptionModule::CreateSession
ms.date: 08/05/2022
targetos: Windows
description: The IMFContentDecryptionModule::CreateSession function creates a IMFContentDecryptionModuleSession object representing a Content Decryption Module (CDM) session.
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
 - IMFContentDecryptionModule::CreateSession
f1_keywords:
 - IMFContentDecryptionModule::CreateSession
 - mfcontentdecryptionmodule/IMFContentDecryptionModule::CreateSession
dev_langs:
 - c++
---

## -description

Creates a [IMFContentDecryptionModuleSession](nn-mfcontentdecryptionmodule-imfcontentdecryptionmodulesession.md) object representing a Content Decryption Module (CDM) session.

## -parameters

### -param sessionType

A member of the [MF_MEDIAKEYSESSION_TYPE](../mfidl/ne-mfidl-mf_mediakeysession_type.md) that specifies the type of CDM session to create.

### -param callbacks

An [IMFContentDecryptionModuleSessionCallbacks](nn-mfcontentdecryptionmodule-imfcontentdecryptionmodulesessioncallbacks.md) object for receiving key status change updates.

### -param session

Receives the created **IMFContentDecryptionModuleSession** object.

## -returns

Returns S_OK on success.

## -remarks

**CreateSession** is based on the Encrypted Media Extension specification's [createSession](https://www.w3.org/TR/2017/REC-encrypted-media-20170918/#dom-mediakeys-createsession).

## -see-also