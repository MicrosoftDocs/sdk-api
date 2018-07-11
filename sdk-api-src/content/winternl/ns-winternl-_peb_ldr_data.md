---
UID: NS:winternl._PEB_LDR_DATA
title: "_PEB_LDR_DATA"
author: windows-sdk-content
description: Contains information about the loaded modules for the process.
old-location: base\peb_ldr_data.htm
old-project: ProcThread
ms.assetid: 2e03b513-5c03-4436-99f8-3a6d3a45aff2
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: "*PPEB_LDR_DATA, PEB_LDR_DATA, PEB_LDR_DATA structure, PPEB_LDR_DATA, PPEB_LDR_DATA structure pointer, _PEB_LDR_DATA, base.peb_ldr_data, winternl/PEB_LDR_DATA, winternl/PPEB_LDR_DATA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: PEB_LDR_DATA, *PPEB_LDR_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winternl.h
api_name:
 - PEB_LDR_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PEB_LDR_DATA structure


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

<pre class="syntax" xml:space="preserve"><code>typedef struct _LIST_ENTRY {
   struct _LIST_ENTRY *Flink;
   struct _LIST_ENTRY *Blink;
} LIST_ENTRY, *PLIST_ENTRY, *RESTRICTED_POINTER PRLIST_ENTRY;</code></pre>
The <b>LDR_DATA_TABLE_ENTRY</b> structure is defined as follows: 

<pre class="syntax" xml:space="preserve"><code>typedef struct _LDR_DATA_TABLE_ENTRY {
    PVOID Reserved1[2];
    LIST_ENTRY InMemoryOrderLinks;
    PVOID Reserved2[2];
    PVOID DllBase;
    PVOID EntryPoint;
    PVOID Reserved3;
    UNICODE_STRING FullDllName;
    BYTE Reserved4[8];
    PVOID Reserved5[3];
    union {
        ULONG CheckSum;
        PVOID Reserved6;
    };
    ULONG TimeDateStamp;
} LDR_DATA_TABLE_ENTRY, *PLDR_DATA_TABLE_ENTRY;
</code></pre>





## -see-also




<a href="https://msdn.microsoft.com/836a6b82-d3e8-4de6-808d-5476dfb51356">PEB</a>
 

 

