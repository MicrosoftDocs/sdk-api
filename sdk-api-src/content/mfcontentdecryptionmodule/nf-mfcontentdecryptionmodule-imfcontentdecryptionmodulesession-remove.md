---
UID: NF:mfcontentdecryptionmodule.IMFContentDecryptionModuleSession.Remove
title: IMFContentDecryptionModuleSession::Remove
ms.date: 11/26/2019
targetos: Windows
description: Removes all licenses and keys associated with the session.
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
 - IMFContentDecryptionModuleSession::Remove
f1_keywords:
 - IMFContentDecryptionModuleSession::Remove
 - mfcontentdecryptionmodule/IMFContentDecryptionModuleSession::Remove
dev_langs:
 - c++
---

## -description

Removes all licenses and keys associated with the session.



## -returns

Returns S_OK on success.

## -remarks

For persistent session types, other session data will be cleared as defined for each session type once a release message acknowledgment is processed by [Update](nf-mfcontentdecryptionmodule-imfcontentdecryptionmodulesession-update.md).


**Remove** is based on the Encrypted Media Extension specification's [MediaKeySession.remove](https://www.w3.org/TR/2017/REC-encrypted-media-20170918/#dom-mediakeysession-remove).

## -see-also

