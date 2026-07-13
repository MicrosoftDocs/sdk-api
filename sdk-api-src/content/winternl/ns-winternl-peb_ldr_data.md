---
UID: NS:winternl._PEB_LDR_DATA
title: PEB_LDR_DATA (winternl.h)
description: Contains information about the loaded modules for the process.
helpviewer_keywords: ["*PPEB_LDR_DATA","PEB_LDR_DATA","PEB_LDR_DATA structure","PPEB_LDR_DATA","PPEB_LDR_DATA structure pointer","base.peb_ldr_data","winternl/PEB_LDR_DATA","winternl/PPEB_LDR_DATA"]
old-location: base\peb_ldr_data.htm
tech.root: backup
ms.assetid: 2e03b513-5c03-4436-99f8-3a6d3a45aff2
ms.date: 12/05/2018
ms.keywords: '*PPEB_LDR_DATA, PEB_LDR_DATA, PEB_LDR_DATA structure, PPEB_LDR_DATA, PPEB_LDR_DATA structure pointer, base.peb_ldr_data, winternl/PEB_LDR_DATA, winternl/PPEB_LDR_DATA'
req.header: winternl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: PEB_LDR_DATA, *PPEB_LDR_DATA
req.redist: 
ms.custom: 24H2
f1_keywords:
 - _PEB_LDR_DATA
 - winternl/_PEB_LDR_DATA
 - PPEB_LDR_DATA
 - winternl/PPEB_LDR_DATA
 - PEB_LDR_DATA
 - winternl/PEB_LDR_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winternl.h
api_name:
 - PEB_LDR_DATA
---

# PEB_LDR_DATA structure


## -description

<p class="CCE_Message">[This structure may be altered in future versions of Windows.]

Contains information about the loaded modules for the process.

## -struct-fields

### -field Reserved1

Reserved for internal use by the operating system.

### -field Reserved2

Reserved for internal use by the operating system.

### -field InMemoryOrderModuleList

The head of a doubly-linked list that contains the loaded modules for the process. Each item in the list is a pointer to an <b>LDR_DATA_TABLE_ENTRY</b> structure. For more information, see Remarks.

## -remarks

The <b>LIST_ENTRY</b> structure is defined as follows: 


``` syntax
typedef struct _LIST_ENTRY {
   struct _LIST_ENTRY *Flink;
   struct _LIST_ENTRY *Blink;
} LIST_ENTRY, *PLIST_ENTRY, *RESTRICTED_POINTER PRLIST_ENTRY;
```

The <b>LDR_DATA_TABLE_ENTRY</b> structure is defined as follows: 


``` syntax
typedef struct _LDR_DATA_TABLE_ENTRY {
    PVOID Reserved1[2];
    LIST_ENTRY InMemoryOrderLinks;
    PVOID Reserved2[2];
    PVOID DllBase;
    PVOID Reserved3[2];
    UNICODE_STRING FullDllName;
    BYTE Reserved4[8];
    PVOID Reserved5[3];
    union
    {
        ULONG CheckSum;
        PVOID Reserved6;
    };
    ULONG TimeDateStamp;
} LDR_DATA_TABLE_ENTRY, *PLDR_DATA_TABLE_ENTRY;

```


## -see-also

<a href="/windows/desktop/api/winternl/ns-winternl-peb">PEB</a>
