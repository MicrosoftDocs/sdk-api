---
UID: NF:mfcontentdecryptionmodule.IMFContentDecryptionModuleSession.GetKeyStatuses
title: IMFContentDecryptionModuleSession::GetKeyStatuses
ms.date: 11/26/2019
ms.topic: language-reference
targetos: Windows
description: Gets a reference to an array of structures that represent the key IDs known to the Content Decryption Module (CDM) session and the current status of the associated key.
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
 - IMFContentDecryptionModuleSession::GetKeyStatuses
f1_keywords:
 - mfcontentdecryptionmodule/IMFContentDecryptionModuleSession::GetKeyStatuses
dev_langs:
 - c++
---

## -description

Gets a reference to an array of structures that represent the key IDs known to the Content Decryption Module (CDM) session and the current status of the associated key. 


## -parameters

### -param keyStatuses

Receives a pointer to an array of [MFMediaKeyStatus](/windows/win32/api/mfidl/ns-mfidl-mfmediakeystatus) structures containing the IDs and statuses of the keys known to the CDM session.

### -param numKeyStatuses

Receives the number of structures present in the *keyStatuses* array.

## -returns

Returns S_OK. If an error occurs, the returned mey status list is empty.

## -remarks

**GetKeyStatuses** is based on the Encrypted Media Extension specification's [MediaKeySession.keyStatuses](https://www.w3.org/TR/2017/REC-encrypted-media-20170918/#dom-mediakeysession-keystatuses).

## -see-also

