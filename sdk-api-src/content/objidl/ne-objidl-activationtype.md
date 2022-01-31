---
UID: NE:objidl.tagACTIVATIONTYPE
title: ACTIVATIONTYPE (objidl.h)
description: Specifies the kind of activation for an activatable class.
helpviewer_keywords: ["ACTIVATIONTYPE","ActivationType","ActivationType enumeration [Windows Runtime]","ActivationType_InProcess","ActivationType_OutOfProcess","ActivationType_RemoteProcess","__x_ABI_CWindows_CFoundation_CActivationType","activationregistration/ActivationType","activationregistration/ActivationType_InProcess","activationregistration/ActivationType_OutOfProcess","activationregistration/ActivationType_RemoteProcess","winrt.activationtype"]
old-location: winrt\activationtype.htm
tech.root: WinRT
ms.assetid: 200257CC-FE26-407F-8AE4-4DB7030AB4E7
ms.date: 12/05/2018
ms.keywords: ACTIVATIONTYPE, ActivationType, ActivationType enumeration [Windows Runtime], ActivationType_InProcess, ActivationType_OutOfProcess, ActivationType_RemoteProcess, __x_ABI_CWindows_CFoundation_CActivationType, activationregistration/ActivationType, activationregistration/ActivationType_InProcess, activationregistration/ActivationType_OutOfProcess, activationregistration/ActivationType_RemoteProcess, winrt.activationtype
req.header: objidl.h
req.include-header: Objidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ACTIVATIONTYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagACTIVATIONTYPE
 - objidl/tagACTIVATIONTYPE
 - ACTIVATIONTYPE
 - objidl/ACTIVATIONTYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - activationregistration.h
api_name:
 - ActivationType
---

# ACTIVATIONTYPE enumeration


## -description

Specifies the kind of activation for an activatable class.

## -enum-fields

### -field ACTIVATIONTYPE_UNCATEGORIZED:0

### -field ACTIVATIONTYPE_FROM_MONIKER:0x1

### -field ACTIVATIONTYPE_FROM_DATA:0x2

### -field ACTIVATIONTYPE_FROM_STORAGE:0x4

### -field ACTIVATIONTYPE_FROM_STREAM:0x8

### -field ACTIVATIONTYPE_FROM_FILE:0x10

#### - ActivationType_InProcess

Specifies in-process activation.


#### - ActivationType_OutOfProcess

Specifies out-of-process activation.


#### - ActivationType_RemoteProcess

Specifies remote-process activation.

## -see-also

<a href="/windows/desktop/api/activationregistration/nn-activationregistration-iactivatableclassregistration">IActivatableClassRegistration</a>
