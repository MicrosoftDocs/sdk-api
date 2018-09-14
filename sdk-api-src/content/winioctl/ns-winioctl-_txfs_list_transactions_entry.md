---
UID: NS:winioctl._TXFS_LIST_TRANSACTIONS_ENTRY
title: "_TXFS_LIST_TRANSACTIONS_ENTRY"
author: windows-sdk-content
description: Contains information about a transaction.
old-location: fs\txfs_list_transactions_entry.htm
tech.root: FileIO
ms.assetid: 7de14fb1-1972-4bf0-b0e2-f0344e963eef
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PTXFS_LIST_TRANSACTIONS_ENTRY, PTXFS_LIST_TRANSACTIONS_ENTRY, PTXFS_LIST_TRANSACTIONS_ENTRY structure pointer [Files], TXFS_LIST_TRANSACTIONS_ENTRY, TXFS_LIST_TRANSACTIONS_ENTRY structure [Files], _TXFS_LIST_TRANSACTIONS_ENTRY, fs.txfs_list_transactions_entry, winioctl/PTXFS_LIST_TRANSACTIONS_ENTRY, winioctl/TXFS_LIST_TRANSACTIONS_ENTRY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - TXFS_LIST_TRANSACTIONS_ENTRY
product: Windows
targetos: Windows
req.typenames: TXFS_LIST_TRANSACTIONS_ENTRY, *PTXFS_LIST_TRANSACTIONS_ENTRY
req.redist: 
---

# _TXFS_LIST_TRANSACTIONS_ENTRY structure


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://msdn.microsoft.com/9ee26e7e-990e-4cd3-8180-f0fcaac2b752">Alternatives to using Transactional NTFS</a>.]

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




<a href="https://msdn.microsoft.com/ff319bf0-2bd4-4824-bf97-b9b6eab90915">FSCTL_TXFS_LIST_TRANSACTIONS</a>



<a href="https://msdn.microsoft.com/4c5ec2eb-f0d9-4603-96d5-1a53e56e97b8">TXFS_LIST_TRANSACTIONS</a>
 

 

