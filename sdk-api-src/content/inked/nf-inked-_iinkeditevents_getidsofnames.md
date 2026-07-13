---
UID: NF:inked._IInkEditEvents_GetIDsOfNames
tech.root: tablet
title: _IInkEditEvents_GetIDsOfNames
ms.date: 02/07/2023
targetos: Windows
description: Maps a set of names to a corresponding set of DISPIDs.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: inked.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - inked.h
api_name:
 - _IInkEditEvents_GetIDsOfNames
f1_keywords:
 - _IInkEditEvents_GetIDsOfNames
 - inked/_IInkEditEvents_GetIDsOfNames
dev_langs:
 - c++
helpviewer_keywords:
 - _IInkEditEvents_GetIDsOfNames
---

# IInkEditEvents_GetIDsOfNames function

## -description

Maps a set of names to a corresponding set of DISPIDs.

## -parameters

### -param This

The [IInkEditEvents interface](nn-inked-_iinkeditevents.md) object.

### -param riid

Reserved. Use IID_NULL.

### -param rgszNames

Address of an array of wide-character strings that contain the names to be mapped.

### -param cNames

Size of the array given by the *rgszNames* parameter.

### -param lcid

Locale context in which to interpret the names. Can be **NULL**.

### -param rgDispId

Pointer to an array that receives the DISPIDs. Each element of receives an identifier that corresponds to one of the names passed in the *rgszNames* parameter.

## -remarks

## -see-also
