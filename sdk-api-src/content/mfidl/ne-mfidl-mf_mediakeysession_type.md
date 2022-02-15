---
UID: NE:mfidl.MF_MEDIAKEYSESSION_TYPE
title: MF_MEDIAKEYSESSION_TYPE
ms.date: 11/4/2019
targetos: Windows
description: Specifies the type of a Content Decryption Module (CDM) session, represented by an IMFContentDecryptionModuleSession object.
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
 - MF_MEDIAKEYSESSION_TYPE
f1_keywords:
 - MF_MEDIAKEYSESSION_TYPE
 - mfidl/MF_MEDIAKEYSESSION_TYPE
dev_langs:
 - c++
---

## -description

Specifies the type of a Content Decryption Module (CDM) session, represented by an [IMFContentDecryptionModuleSession](../mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodulesession.md) object.

## -enum-fields

### -field MF_MEDIAKEYSESSION_TYPE_TEMPORARY:0

A session for which the license, key(s) and record of or data related to the session are not persisted.

### -field MF_MEDIAKEYSESSION_TYPE_PERSISTENT_LICENSE

A session for which the license (and potentially other data related to the session) will be persisted.

### -field MF_MEDIAKEYSESSION_TYPE_PERSISTENT_RELEASE_MESSAGE

A record of license destruction.

### -field MF_MEDIAKEYSESSION_TYPE_PERSISTENT_USAGE_RECORD

A record of license usage.

## -remarks

Pass a member of this enumeration into [IMFContentDecryptionModule::CreateSession](../mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmodule-createsession.md)

## -see-also

- IMFContentDecryptionModuleSession](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodulesession)

- [IMFContentDecryptionModule::CreateSession](../mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmodule-createsession.md)
