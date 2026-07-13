---
UID: NE:mfidl.MF_MEDIAKEY_STATUS
title: MF_MEDIAKEY_STATUS
ms.date: 11/4/2019
targetos: Windows
description: Specifies the status of a Content Decryption Module (CDM) session key.
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
 - MF_MEDIAKEY_STATUS
f1_keywords:
 - MF_MEDIAKEY_STATUS
 - mfidl/MF_MEDIAKEY_STATUS
dev_langs:
 - c++
---

## -description

Specifies the status of a Content Decryption Module (CDM) session key.

## -enum-fields

### -field MF_MEDIAKEY_STATUS_USABLE:0

The CDM is certain the key is currently usable for decryption.

### -field MF_MEDIAKEY_STATUS_EXPIRED

The key is no longer usable for decryption because its expiration time has passed.

### -field MF_MEDIAKEY_STATUS_OUTPUT_DOWNSCALED

There are output restrictions associated with the key that cannot currently be met. Media data decrypted with this key may be presented at a lower quality (e.g., resolution), if necessary according to the output restrictions.

### -field MF_MEDIAKEY_STATUS_OUTPUT_NOT_ALLOWED

There are output restrictions associated with the key that disallow output.

### -field MF_MEDIAKEY_STATUS_STATUS_PENDING

The status of the key is not yet known and is being determined. The status will be updated with the actual status when it has been determined.

### -field MF_MEDIAKEY_STATUS_INTERNAL_ERROR

The key is not currently usable for decryption because of an error in the CDM unrelated to the other values. This value is not actionable by the application.

### -field MF_MEDIAKEY_STATUS_RELEASED

The key itself is no longer available to the CDM, but information about the key, such as a record of license destruction, is available.

### -field MF_MEDIAKEY_STATUS_OUTPUT_RESTRICTED

There are output restrictions associated with the key that cannot currently be met. Media data decrypted with this key may be blocked from presentation, if necessary according to the output restrictions. The application should avoid using streams that will trigger the output restrictions associated with the key.

## -remarks

This enumeration is with the [MFMediaKeyStatus](ns-mfidl-mfmediakeystatus.md) structure used as the output parameter for the [IMFContentDecryptionModuleSession::GetKeyStatuses](../mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmodulesession-getkeystatuses.md) method.


**MF_MEDIAKEY_STATUS** is based on the Encrypted Media Extension specification's [MediaKeyStatus](https://www.w3.org/TR/2017/REC-encrypted-media-20170918/#dom-mediakeystatus) enumeration.

## -see-also

* [MFMediaKeyStatus](ns-mfidl-mfmediakeystatus.md)
* [IMFContentDecryptionModuleSession::GetKeyStatuses](../mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmodulesession-getkeystatuses.md)
