---
UID: NF:mfcontentdecryptionmodule.IMFContentDecryptionModule.SetPMPHostApp
title: IMFContentDecryptionModule::SetPMPHostApp
ms.date: 11/26/2019
targetos: Windows
description: Allows the caller to specify the IMFPMPHostApp interface, which represents a protected process.
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
 - IMFContentDecryptionModule::SetPMPHostApp
f1_keywords:
 - IMFContentDecryptionModule::SetPMPHostApp
 - mfcontentdecryptionmodule/IMFContentDecryptionModule::SetPMPHostApp
dev_langs:
 - c++
---

## -description

Allows the caller to specify the [IMFPMPHostApp](../mfidl/nn-mfidl-imfpmphostapp.md) interface, which represents a protected process. The **IMFPMPHostApp** interface is used by the Content Decryption Module (CDM) to create the IMFTrustedInput object.

## -parameters

### -param pmpHostApp

The **IMFPMPHostApp** representing a protected process.

## -returns

Returns S_OK on success.

## -remarks

## -see-also