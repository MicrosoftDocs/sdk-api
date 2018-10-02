---
UID: NS:ntdef._SINGLE_LIST_ENTRY
title: "_SINGLE_LIST_ENTRY"
author: windows-sdk-content
description: A SINGLE_LIST_ENTRY structure describes an entry in a singly linked list, or serves as the header for such a list.
old-location: kernel\single_list_entry.htm
tech.root: Kernel
ms.assetid: 2db8ce7e-67e0-43e8-98b5-a2112db5bd5a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PSINGLE_LIST_ENTRY, PSINGLE_LIST_ENTRY, PSINGLE_LIST_ENTRY structure pointer [Kernel-Mode Driver Architecture], SINGLE_LIST_ENTRY, SINGLE_LIST_ENTRY structure [Kernel-Mode Driver Architecture], _SINGLE_LIST_ENTRY, kernel.single_list_entry, kstruct_d_146e3fe9-b909-4cd8-9eba-61203c32d658.xml, ntdef/PSINGLE_LIST_ENTRY, ntdef/SINGLE_LIST_ENTRY"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntdef.h
api_name:
 - SINGLE_LIST_ENTRY
product: Windows
targetos: Windows
req.typenames: SINGLE_LIST_ENTRY, *PSINGLE_LIST_ENTRY
req.redist: 
---

# _SINGLE_LIST_ENTRY structure


## -description


A <b>SINGLE_LIST_ENTRY</b> structure describes an entry in a singly linked list, or serves as the header for such a list.


## -struct-fields




### -field Next

For a <b>SINGLE_LIST_ENTRY</b> that serves as a list entry, the <b>Next</b> member points to the next entry in the list, or <b>NULL</b> if there is no next entry in the list. For a <b>SINGLE_LIST_ENTRY</b> that serves as the list header, the <b>Next</b> member points to the first entry in the list, or <b>NULL</b> if the list is empty.


## -remarks



If a <b>SINGLE_LIST_ENTRY</b> structure is used as a list head, initialize the <b>Next</b> member of the structure to be <b>NULL</b>.

A driver can access the <b>Next</b> member of a <b>SINGLE_LIST_ENTRY</b>, but (other than initializing a list head) <b>Next</b> must only be updated by the system routines supplied for this purpose.

For more information about how to use <b>SINGLE_LIST_ENTRY</b> structures to implement a singly linked list, see <a href="https://msdn.microsoft.com/3a305f54-7866-4163-a3e4-e078d1927adc">Singly and Doubly Linked Lists</a>.




## -see-also




<a href="https://msdn.microsoft.com/339e688f-64ec-402f-bd28-9fa487acb984">ExInterlockedPopEntryList</a>



<a href="https://msdn.microsoft.com/7a932f69-c5dd-4844-b461-b986c00a08c7">ExInterlockedPushEntryList</a>



<a href="https://msdn.microsoft.com/b24ec573-4164-4016-a19d-574ebd75ec8f">PopEntryList</a>



<a href="https://msdn.microsoft.com/19f387d3-6c00-4c71-8114-61c53654613c">PushEntryList</a>
 

 

