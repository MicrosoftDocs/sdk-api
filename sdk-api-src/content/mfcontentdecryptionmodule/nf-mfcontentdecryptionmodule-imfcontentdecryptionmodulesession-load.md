---
UID: NF:mfcontentdecryptionmodule.IMFContentDecryptionModuleSession.Load
title: IMFContentDecryptionModuleSession::Load
ms.date: 08/05/2022
targetos: Windows
description: The IMFContentDecryptionModuleSession::Load function loads the data for the specified session into the IMFContentDecryptionModuleSession object.
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
 - IMFContentDecryptionModuleSession::Load
f1_keywords:
 - IMFContentDecryptionModuleSession::Load
 - mfcontentdecryptionmodule/IMFContentDecryptionModuleSession::Load
dev_langs:
 - c++
---

## -description

Loads the data for the specified session into the **IMFContentDecryptionModuleSession** object.

## -parameters

### -param sessionId

The unique identifier of the session to load.

### -param loaded

Receives a pointer to a *BOOL* indicating if the session data was loaded successfully.

## -returns

Returns S_OK.

## -remarks

**Load** is based on the Encrypted Media Extension specification's [MediaKeySession.Load](https://www.w3.org/TR/2017/REC-encrypted-media-20170918/#dom-mediakeysession-load).

## -see-also

