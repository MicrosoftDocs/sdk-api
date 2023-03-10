---
UID: NE:minidumpapiset._MINIDUMP_HANDLE_OBJECT_INFORMATION_TYPE
title: MINIDUMP_HANDLE_OBJECT_INFORMATION_TYPE (minidumpapiset.h)
description: Identifies the type of object-specific information.
helpviewer_keywords: ["MINIDUMP_HANDLE_OBJECT_INFORMATION_TYPE","MINIDUMP_HANDLE_OBJECT_INFORMATION_TYPE enumeration","MiniHandleObjectInformationNone","MiniMutantInformation1","MiniMutantInformation2","MiniProcessInformation1","MiniProcessInformation2","MiniThreadInformation1","base.minidump_handle_object_information_type","minidumpapiset/MINIDUMP_HANDLE_OBJECT_INFORMATION_TYPE","minidumpapiset/MiniHandleObjectInformationNone","minidumpapiset/MiniMutantInformation1","minidumpapiset/MiniMutantInformation2","minidumpapiset/MiniProcessInformation1","minidumpapiset/MiniProcessInformation2","minidumpapiset/MiniThreadInformation1"]
old-location: base\minidump_handle_object_information_type.htm
tech.root: Debug
ms.assetid: 255023e3-0412-42c8-ae80-eba5f00af5ff
ms.date: 12/05/2018
ms.keywords: MINIDUMP_HANDLE_OBJECT_INFORMATION_TYPE, MINIDUMP_HANDLE_OBJECT_INFORMATION_TYPE enumeration, MiniHandleObjectInformationNone, MiniMutantInformation1, MiniMutantInformation2, MiniProcessInformation1, MiniProcessInformation2, MiniThreadInformation1, base.minidump_handle_object_information_type, minidumpapiset/MINIDUMP_HANDLE_OBJECT_INFORMATION_TYPE, minidumpapiset/MiniHandleObjectInformationNone, minidumpapiset/MiniMutantInformation1, minidumpapiset/MiniMutantInformation2, minidumpapiset/MiniProcessInformation1, minidumpapiset/MiniProcessInformation2, minidumpapiset/MiniThreadInformation1
req.header: minidumpapiset.h
req.include-header: DbgHelp.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: MINIDUMP_HANDLE_OBJECT_INFORMATION_TYPE
req.redist: DbgHelp.dll 6.5 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_HANDLE_OBJECT_INFORMATION_TYPE
 - minidumpapiset/_MINIDUMP_HANDLE_OBJECT_INFORMATION_TYPE
 - MINIDUMP_HANDLE_OBJECT_INFORMATION_TYPE
 - minidumpapiset/MINIDUMP_HANDLE_OBJECT_INFORMATION_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_HANDLE_OBJECT_INFORMATION_TYPE
---

# MINIDUMP_HANDLE_OBJECT_INFORMATION_TYPE enumeration


## -description

Identifies the type of object-specific information.

## -enum-fields

### -field MiniHandleObjectInformationNone

There is no object-specific information for this handle type.

### -field MiniThreadInformation1

The information is specific to thread objects.

### -field MiniMutantInformation1

The information is specific to mutant objects.

### -field MiniMutantInformation2

The information is specific to mutant objects.

### -field MiniProcessInformation1

The information is specific to process objects.

### -field MiniProcessInformation2

The information is specific to process objects.

### -field MiniEventInformation1

### -field MiniSectionInformation1

### -field MiniSemaphoreInformation1

### -field MiniHandleObjectInformationTypeMax

## -remarks

The information represented by each of these values can vary by operating system and procesor architecture. Per-handle object-specific information is automatically gathered when minidump type is MiniDumpWithHandleData. For more information, see <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type">MINIDUMP_TYPE</a>.

## -see-also

<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_handle_object_information">MINIDUMP_HANDLE_OBJECT_INFORMATION</a>