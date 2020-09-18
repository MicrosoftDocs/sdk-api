---
UID: NS:winioctl._TXFS_LIST_TRANSACTIONS_ENTRY
title: TXFS_LIST_TRANSACTIONS_ENTRY
description: Contains information about a transaction.
helpviewer_keywords: ["*PTXFS_LIST_TRANSACTIONS_ENTRY","PTXFS_LIST_TRANSACTIONS_ENTRY","PTXFS_LIST_TRANSACTIONS_ENTRY structure pointer [Files]","TXFS_LIST_TRANSACTIONS_ENTRY","TXFS_LIST_TRANSACTIONS_ENTRY structure [Files]","fs.txfs_list_transactions_entry","winioctl/PTXFS_LIST_TRANSACTIONS_ENTRY","winioctl/TXFS_LIST_TRANSACTIONS_ENTRY"]
old-location: fs\txfs_list_transactions_entry.htm
tech.root: fs
ms.assetid: 7de14fb1-1972-4bf0-b0e2-f0344e963eef
ms.date: 12/05/2018
ms.keywords: '*PTXFS_LIST_TRANSACTIONS_ENTRY, PTXFS_LIST_TRANSACTIONS_ENTRY, PTXFS_LIST_TRANSACTIONS_ENTRY structure pointer [Files], TXFS_LIST_TRANSACTIONS_ENTRY, TXFS_LIST_TRANSACTIONS_ENTRY structure [Files], fs.txfs_list_transactions_entry, winioctl/PTXFS_LIST_TRANSACTIONS_ENTRY, winioctl/TXFS_LIST_TRANSACTIONS_ENTRY'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: TXFS_LIST_TRANSACTIONS_ENTRY, *PTXFS_LIST_TRANSACTIONS_ENTRY
req.redist: 
f1_keywords:
 - _TXFS_LIST_TRANSACTIONS_ENTRY
 - winioctl/_TXFS_LIST_TRANSACTIONS_ENTRY
 - PTXFS_LIST_TRANSACTIONS_ENTRY
 - winioctl/PTXFS_LIST_TRANSACTIONS_ENTRY
 - TXFS_LIST_TRANSACTIONS_ENTRY
 - winioctl/TXFS_LIST_TRANSACTIONS_ENTRY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - TXFS_LIST_TRANSACTIONS_ENTRY
---

# TXFS_LIST_TRANSACTIONS_ENTRY structure


## -description

<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Contains information about a transaction.

## -struct-fields

### -field TransactionId

The GUID of the transaction.

### -field TransactionState

The current state of the transaction.

### -field Reserved1

Reserved.

### -field Reserved2

Reserved.

### -field Reserved3

Reserved.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_txfs_list_transactions">FSCTL_TXFS_LIST_TRANSACTIONS</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-txfs_list_transactions">TXFS_LIST_TRANSACTIONS</a>