---
UID: NF:mfcontentdecryptionmodule.MFCreateEncryptedMediaExtensionsStoreActivate
title: MFCreateEncryptedMediaExtensionsStoreActivate
ms.date: 08/05/2022
targetos: Windows
description: The MFCreateEncryptedMediaExtensionsStoreActivate function creates an object that implements IMFActivate. This object’s implementation of ActivateObject is based on the specified IMFPMPHostApp and class ID.
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
req.lib: Mf.lib
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
api_location:
 - mfcontentdecryptionmodule.h
api_name:
 - MFCreateEncryptedMediaExtensionsStoreActivate
f1_keywords:
 - MFCreateEncryptedMediaExtensionsStoreActivate
 - mfcontentdecryptionmodule/MFCreateEncryptedMediaExtensionsStoreActivate
dev_langs:
 - c++
---

## -description

This function creates an object that implements [IMFActivate](../mfobjects/nn-mfobjects-imfactivate.md). This object’s implementation of ActivateObject is based on the specified IMFPMPHostApp and class ID.

## -parameters

### -param pmpHost

An [IMFPMPHostApp](../mfidl/nn-mfidl-imfpmphostapp.md) with the necessary information to create the **IMFActivate** for this app package.

### -param objectStream

An [IStream](../objidl/nn-objidl-istream.md) representing the object stream that will be loaded via IMFActivate::Load.

### -param classId

An **LPCWSTR** representing the target object's activatable class id.

### -param activate

Receives a reference to the to an **IMFActivate**.

## -returns

Returns S_OK on success.

## -remarks

The **IMFActivate** can be created in a protected process and activated in an app process.

## -see-also