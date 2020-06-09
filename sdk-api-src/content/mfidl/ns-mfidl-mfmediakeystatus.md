---
UID: NS:mfidl.MFMediaKeyStatus
title: MFMediaKeyStatus
ms.date: 11/4/2019
ms.topic: language-reference
targetos: Windows
description: Reporesents the status of a Content Decryption Module (CDM) session key.
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: mfidl.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.typenames: MFMediaKeyStatus
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFMediaKeyStatus
f1_keywords:
 - mfidl/MFMediaKeyStatus
dev_langs:
 - c++
---

## -description

Reporesents the status of a Content Decryption Module (CDM) session key.

## -struct-fields

### -field pbKeyId

A byte array representing the identifier of a session key.

### -field cbKeyId

The number of bytes in the *pbKeyId* paramater.

### -field eMediaKeyStatus

A value from the [MF_MEDIAKEY_STATUS](ne-mfidl-mf_mediakey_status) enumeration specifying the status of the associated session key.

## -remarks

This structure is used as the output parameter for the [IMFContentDecryptionModuleSession::GetKeyStatuses](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmodulesession-getkeystatuses) method.

**MFMediaKeyStatus** is based on the Encrypted Media Extension specification's [MediaKeyStatusMap](https://www.w3.org/TR/2017/REC-encrypted-media-20170918/#dom-mediakeysession-sessionid).

## -see-also

