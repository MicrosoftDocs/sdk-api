---
UID: NF:interlockedapi.InterlockedPushListSListEx
title: InterlockedPushListSListEx function (interlockedapi.h)
description: Inserts a singly-linked list at the front of another singly linked list. Access to the lists is synchronized on a multiprocessor system. This version of the method does not use the __fastcall calling convention.
helpviewer_keywords: ["InterlockedPushListSListEx","InterlockedPushListSListEx function","base.interlockedpushlistslistex","interlockedapi/InterlockedPushListSListEx"]
old-location: base\interlockedpushlistslistex.htm
tech.root: backup
ms.assetid: f4f334c6-fda8-4c5f-9177-b672c8aed6b3
ms.date: 02/05/2024
ms.keywords: InterlockedPushListSListEx, InterlockedPushListSListEx function, base.interlockedpushlistslistex, interlockedapi/InterlockedPushListSListEx
req.header: interlockedapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InterlockedPushListSListEx
 - interlockedapi/InterlockedPushListSListEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-interlocked-l1-2-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - vertdll.dll
api_name:
 - InterlockedPushListSListEx
---

# InterlockedPushListSListEx function

## -description

Inserts a singly-linked list at the front of another singly linked list. Access to the lists is synchronized on a multiprocessor system. This version of the method does not use the [__fastcall](/previous-versions/6xa169sk(v=vs.85)) calling convention.

## -parameters

### -param ListHead [in, out]

Pointer to an **SLIST_HEADER** structure that represents the head of a singly linked list. The list specified by the *List* and *ListEnd* parameters is inserted at the front of this list.

### -param List [in, out]

Pointer to an [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) structure that represents the first item in the  list to be inserted.

### -param ListEnd [in, out]

Pointer to an [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) structure that represents the last item in the  list to be inserted.

### -param Count [in]

The number of items in the list to be inserted.

## -returns

The return value is the previous first item in the list specified by the *ListHead* parameter. If the list was previously empty, the return value is `NULL`.

## -remarks

All list items must be aligned on a **MEMORY_ALLOCATION_ALIGNMENT** boundary; otherwise, this function will behave unpredictably. See **_aligned_malloc**.

## -see-also

[Interlocked Singly Linked Lists](/windows/win32/Sync/interlocked-singly-linked-lists)

[InterlockedFlushSList](nf-interlockedapi-interlockedflushslist.md)

[InterlockedPopEntrySList](nf-interlockedapi-interlockedpopentryslist.md)

[InterlockedPushEntrySList](nf-interlockedapi-interlockedpushentryslist.md)

[SLIST_ENTRY](../winnt/ns-winnt-slist_entry.md)

[Using Singly Linked Lists](/windows/win32/Sync/using-singly-linked-lists)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
