---
UID: NF:mfcontentdecryptionmodule.IMFContentDecryptionModule.GetSuspendNotify
title: IMFContentDecryptionModule::GetSuspendNotify
ms.date: 11/26/2019
targetos: Windows
description: Retrieves an object for IMFContentDecryptionModuleSession suspend events.
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
 - IMFContentDecryptionModule::GetSuspendNotify
f1_keywords:
 - IMFContentDecryptionModule::GetSuspendNotify
 - mfcontentdecryptionmodule/IMFContentDecryptionModule::GetSuspendNotify
dev_langs:
 - c++
---

## -description

Retrieves an object for [IMFContentDecryptionModuleSession](nn-mfcontentdecryptionmodule-imfcontentdecryptionmodulesession.md) suspend events.

## -parameters

### -param notify

Receives an [IMFCdmSuspendNotify](../mfmediaengine/nn-mfmediaengine-imfcdmsuspendnotify.md) object that notifies the Content Decryption Module (CDM) when global resources should be brought into a consistent state prior to suspending.

## -returns

Returns S_OK on success.

## -remarks

## -see-also