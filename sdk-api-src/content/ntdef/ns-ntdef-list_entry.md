---
UID: NS:ntdef._LIST_ENTRY
title: LIST_ENTRY (ntdef.h)

description: A LIST_ENTRY structure describes an entry in a doubly linked list or serves as the header for such a list.
old-location: kernel\list_entry.htm
tech.root: Kernel
ms.assetid: f3c1867b-4d7e-4935-a902-b7cf54534655

ms.date: 12/05/2018
ms.keywords: "*PLIST_ENTRY, LIST_ENTRY, LIST_ENTRY structure [Kernel-Mode Driver Architecture], PLIST_ENTRY, PLIST_ENTRY structure pointer [Kernel-Mode Driver Architecture], PRLIST_ENTRY, kernel.list_entry, kstruct_c_1bef4e3c-4fcc-47e3-8e95-b5a697b720a2.xml, ntdef/LIST_ENTRY, ntdef/PLIST_ENTRY"
ms.topic: struct
f1_keywords: 
 - "ntdef/LIST_ENTRY"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: LIST_ENTRY, *PLIST_ENTRY, PRLIST_ENTRY
req.redist: 
ms.custom: 19H1
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



A <b>LIST_ENTRY</b> structure that describes the list head must have been initialized by calling <a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/wdm/nf-wdm-initializelisthead">InitializeListHead</a>.

A driver can access the <b>Flink</b> or <b>Blink</b> members of a <b>LIST_ENTRY</b>, but the members must only be updated by the system routines supplied for this purpose.

For more information about how to use <b>LIST_ENTRY</b> structures to implement a doubly linked list, see <a href="https://docs.microsoft.com/windows-hardware/drivers/kernel/singly-and-doubly-linked-lists">Singly and Doubly Linked Lists</a>.




## -see-also




<a href="https://msdn.microsoft.com/91640a96-abad-424e-b9bd-301dad2b6aac">ExInterlockedInsertHeadList</a>



<a href="https://msdn.microsoft.com/cd322d64-4005-426c-b3ce-0fe8f6ce868e">ExInterlockedInsertTailList</a>



<a href="https://msdn.microsoft.com/d024da2c-9629-4907-98b8-a29dc6022ac0">ExInterlockedRemoveHeadList</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/wdm/nf-wdm-initializelisthead">InitializeListHead</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/wdm/nf-wdm-insertheadlist">InsertHeadList</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/wdm/nf-wdm-inserttaillist">InsertTailList</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/wdm/nf-wdm-islistempty">IsListEmpty</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/wdm/nf-wdm-removeentrylist">RemoveEntryList</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/wdm/nf-wdm-removeheadlist">RemoveHeadList</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/wdm/nf-wdm-removetaillist">RemoveTailList</a>
 

 

