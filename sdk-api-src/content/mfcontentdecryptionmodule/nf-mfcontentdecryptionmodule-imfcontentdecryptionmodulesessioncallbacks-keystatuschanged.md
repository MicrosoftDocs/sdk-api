---
UID: NF:mfcontentdecryptionmodule.IMFContentDecryptionModuleSessionCallbacks.KeyStatusChanged
title: IMFContentDecryptionModuleSessionCallbacks::KeyStatusChanged
ms.date: 08/05/2022
targetos: Windows
description: The IMFContentDecryptionModuleSessionCallbacks::KeyStatusChanged function is called when there has been a change in the keys in the Content Decryption Module (CDM) session or their status.
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
 - IMFContentDecryptionModuleSessionCallbacks::KeyStatusChanged
f1_keywords:
 - IMFContentDecryptionModuleSessionCallbacks::KeyStatusChanged
 - mfcontentdecryptionmodule/IMFContentDecryptionModuleSessionCallbacks::KeyStatusChanged
dev_langs:
 - c++
---

## -description

Called when there has been a change in the keys in the Content Decryption Module (CDM) session or their status.



## -returns

Returns S_OK.

## -remarks

Get the current status of the CDM session keys by calling [IMFContentDecryptionModuleSession::GetKeyStatuses](nf-mfcontentdecryptionmodule-imfcontentdecryptionmodulesession-getkeystatuses.md). 

**KeyStatusChanged** is based on the Encrypted Media Extension specification's [keystatuseschange](https://www.w3.org/TR/2017/REC-encrypted-media-20170918/#dom-evt-keystatuseschange).

## -see-also

