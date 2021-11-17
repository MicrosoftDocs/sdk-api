---
UID: NF:wabiab.IAddrBook.CompareEntryIDs
tech.root: wab wab 
title: IAddrBook::CompareEntryIDs
ms.date: 03/03/2021
ms.topic: language-reference
targetos: Windows
description: Compares two entry identifiers.
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
 - IAddrBook::CompareEntryIDs
f1_keywords:
 - IAddrBook::CompareEntryIDs
 - wabiab/IAddrBook::CompareEntryIDs
dev_langs:
 - c++
---

## -description

Compares two entry identifiers.

## -parameters

### -param cbEntryID1

Value of type ULONG that specifies the number of bytes in the entry identifier to which the *lpEntryID1* parameter points.

### -param lpEntryID1

Pointer to a variable of type ENTRYID that specifies the first entry identifier to be compared.

### -param cbEntryID2

Value of type ULONG that specifies the number of bytes in the entry identifier to which the *lpEntryID2* parameter points.

### -param lpEntryID2

Pointer to a variable of type ENTRYID that specifies the first entry identifier to be compared.


### -param ulFlags

Reserved. Must be set to 0.

### -param lpulResult

Pointer to a variable of type ULONG that receives the result of the comparison. The contents of *lpulResult* are set to TRUE if the two entry identifiers refer to the same object, FALSE otherwise.

## -returns

HRESULT

## -remarks

## -see-also

