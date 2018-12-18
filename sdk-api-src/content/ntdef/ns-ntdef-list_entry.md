---
UID: NS:ntdef._LIST_ENTRY
title: LIST_ENTRY
author: windows-sdk-content
description: A LIST_ENTRY structure describes an entry in a doubly linked list or serves as the header for such a list.
old-location: kernel\list_entry.htm
tech.root: Kernel
ms.assetid: f3c1867b-4d7e-4935-a902-b7cf54534655
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PLIST_ENTRY, LIST_ENTRY, LIST_ENTRY structure [Kernel-Mode Driver Architecture], PLIST_ENTRY, PLIST_ENTRY structure pointer [Kernel-Mode Driver Architecture], PRLIST_ENTRY, kernel.list_entry, kstruct_c_1bef4e3c-4fcc-47e3-8e95-b5a697b720a2.xml, ntdef/LIST_ENTRY, ntdef/PLIST_ENTRY"
ms.topic: struct
req.header: ntdef.h
req.include-header: Wdm.h, Ntddk.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntdef.h
api_name:
 - LIST_ENTRY
product: Windows
targetos: Windows
req.typenames: LIST_ENTRY, *PLIST_ENTRY, PRLIST_ENTRY
req.redist: 
---

# LIST_ENTRY structure


## -description


A <b>LIST_ENTRY</b> structure describes an entry in a doubly linked list or serves as the header for such a list.


## -struct-fields




### -field Flink

For a <b>LIST_ENTRY</b> structure that serves as a list entry, the <b>Flink</b> member points to the next entry in the list or to the list header if there is no next entry in the list. 

For a <b>LIST_ENTRY</b> structure that serves as the list header, the <b>Flink</b> member points to the first entry in the list or to the LIST_ENTRY structure itself if the list is empty.


### -field Blink

For a <b>LIST_ENTRY</b> structure that serves as a list entry, the <b>Blink</b> member points to the previous entry in the list or to the list header if there is no previous entry in the list.

For a <b>LIST_ENTRY</b> structure that serves as the list header, the <b>Blink</b> member points to the last entry in the list or to the <b>LIST_ENTRY</b> structure itself if the list is empty.


## -remarks



A <b>LIST_ENTRY</b> structure that describes the list head must have been initialized by calling <a href="https://msdn.microsoft.com/123434fd-4e83-4042-834b-1eb4cf13dd10">InitializeListHead</a>.

A driver can access the <b>Flink</b> or <b>Blink</b> members of a <b>LIST_ENTRY</b>, but the members must only be updated by the system routines supplied for this purpose.

For more information about how to use <b>LIST_ENTRY</b> structures to implement a doubly linked list, see <a href="https://msdn.microsoft.com/3a305f54-7866-4163-a3e4-e078d1927adc">Singly and Doubly Linked Lists</a>.




## -see-also




<a href="https://msdn.microsoft.com/91640a96-abad-424e-b9bd-301dad2b6aac">ExInterlockedInsertHeadList</a>



<a href="https://msdn.microsoft.com/cd322d64-4005-426c-b3ce-0fe8f6ce868e">ExInterlockedInsertTailList</a>



<a href="https://msdn.microsoft.com/d024da2c-9629-4907-98b8-a29dc6022ac0">ExInterlockedRemoveHeadList</a>



<a href="https://msdn.microsoft.com/123434fd-4e83-4042-834b-1eb4cf13dd10">InitializeListHead</a>



<a href="https://msdn.microsoft.com/c3ad9d93-93e1-406b-9a58-26dcbf428b50">InsertHeadList</a>



<a href="https://msdn.microsoft.com/9eb470c8-ee37-497e-982e-d32b4b9b7348">InsertTailList</a>



<a href="https://msdn.microsoft.com/6e494112-a808-4914-8194-e68a2799c38e">IsListEmpty</a>



<a href="https://msdn.microsoft.com/84c3937f-8042-4b15-b5bb-884d14a97a8c">RemoveEntryList</a>



<a href="https://msdn.microsoft.com/8748451c-3e57-4acf-b1e6-b80fe7f461d8">RemoveHeadList</a>



<a href="https://msdn.microsoft.com/67942bf7-28f6-4b2d-a880-9439afaf0bb2">RemoveTailList</a>
 

 

