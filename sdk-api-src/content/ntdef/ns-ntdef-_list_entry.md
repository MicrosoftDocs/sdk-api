---
UID: NS:ntdef._LIST_ENTRY
title: "_LIST_ENTRY"
author: windows-sdk-content
description: A LIST_ENTRY structure describes an entry in a doubly linked list or serves as the header for such a list.
old-location: kernel\list_entry.htm
old-project: kernel
ms.assetid: f3c1867b-4d7e-4935-a902-b7cf54534655
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PLIST_ENTRY, LIST_ENTRY, LIST_ENTRY structure [Kernel-Mode Driver Architecture], PLIST_ENTRY, PLIST_ENTRY structure pointer [Kernel-Mode Driver Architecture], PRLIST_ENTRY, _LIST_ENTRY, kernel.list_entry, kstruct_c_1bef4e3c-4fcc-47e3-8e95-b5a697b720a2.xml, ntdef/LIST_ENTRY, ntdef/PLIST_ENTRY"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: LIST_ENTRY, *PLIST_ENTRY, PRLIST_ENTRY
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
req.lib: 
req.dll: 
req.irql: Any level
req.product: Rights Management Services client 1.0 or later
---

# _LIST_ENTRY structure


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



A <b>LIST_ENTRY</b> structure that describes the list head must have been initialized by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff547799">InitializeListHead</a>.

A driver can access the <b>Flink</b> or <b>Blink</b> members of a <b>LIST_ENTRY</b>, but the members must only be updated by the system routines supplied for this purpose.

For more information about how to use <b>LIST_ENTRY</b> structures to implement a doubly linked list, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff563802">Singly and Doubly Linked Lists</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545397">ExInterlockedInsertHeadList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff545402">ExInterlockedInsertTailList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff545427">ExInterlockedRemoveHeadList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff547799">InitializeListHead</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff547820">InsertHeadList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff547823">InsertTailList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551789">IsListEmpty</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff561029">RemoveEntryList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff561032">RemoveHeadList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff561036">RemoveTailList</a>
 

 

