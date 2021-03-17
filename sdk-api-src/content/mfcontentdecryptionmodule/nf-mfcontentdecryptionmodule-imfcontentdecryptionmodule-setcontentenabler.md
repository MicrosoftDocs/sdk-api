---
UID: NF:mfcontentdecryptionmodule.IMFContentDecryptionModule.SetContentEnabler
title: IMFContentDecryptionModule::SetContentEnabler
ms.date: 11/26/2019
targetos: Windows
description: Allows the caller to specify the IMFContentEnabler interface that shall be used by the Content Decryption Module (CDM).
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
 - IMFContentDecryptionModule::SetContentEnabler
f1_keywords:
 - IMFContentDecryptionModule::SetContentEnabler
 - mfcontentdecryptionmodule/IMFContentDecryptionModule::SetContentEnabler
dev_langs:
 - c++
---

## -description

Allows the caller to specify the [IMFContentEnabler](../mfidl/nn-mfidl-imfcontentenabler.md) interface that shall be used by the Content Decryption Module (CDM).

## -parameters

### -param contentEnabler

The [IMFContentEnabler](../mfidl/nn-mfidl-imfcontentenabler.md) interface to be used by the CDM.

### -param result

An [IMFAsyncResult](../mfobjects/nn-mfobjects-imfasyncresult.md) that provides information about the result of the operation.

## -returns

Returns S_OK on success.

## -remarks

The IMFContentEnabler is typically obtained by calling  [IMFInputTrustAuthority::RequestAccess](../mfidl/nf-mfidl-imfinputtrustauthority-requestaccess.md).

## -see-also