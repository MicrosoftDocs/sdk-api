---
UID: NF:wabiab.IAddrBook.PrepareRecips
tech.root: wab wab 
title: IAddrBook::PrepareRecips
ms.date: 03/03/2021
ms.topic: language-reference
targetos: Windows
description: Prepares a recipient list for later use by the messaging system.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: wabiab.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - wabiab.h
api_name:
 - IAddrBook::PrepareRecips
f1_keywords:
 - IAddrBook::PrepareRecips
 - wabiab/IAddrBook::PrepareRecips
dev_langs:
 - c++
---

## -description

Prepares a recipient list for later use by the messaging system.

## -parameters

### -param ulFlags

Reserved. Must be set to 0.

### -param lpPropTagArray

Pointer to a variable of type **SPropTagArray** that specifies an array of property tags indicating properties that require updating, if any. The variable can be NULL.

### -param lpRecipList

Pointer to a variable of type **ADRLIST** that specifies the structure holding the list of recipients.

## -returns

## -remarks

## -see-also

