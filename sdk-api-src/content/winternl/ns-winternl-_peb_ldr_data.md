---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

