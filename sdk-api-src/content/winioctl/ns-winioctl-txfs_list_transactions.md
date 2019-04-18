---
UID: NS:winioctl._TXFS_LIST_TRANSACTIONS
title: TXFS_LIST_TRANSACTIONS (winioctl.h)
author: windows-sdk-content
description: Contains a list of transactions.
old-location: fs\txfs_list_transactions.htm
tech.root: FileIO
ms.assetid: 4c5ec2eb-f0d9-4603-96d5-1a53e56e97b8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PTXFS_LIST_TRANSACTIONS, PTXFS_LIST_TRANSACTIONS, PTXFS_LIST_TRANSACTIONS structure pointer [Files], TXFS_LIST_TRANSACTIONS, TXFS_LIST_TRANSACTIONS structure [Files], fs.txfs_list_transactions, winioctl/PTXFS_LIST_TRANSACTIONS, winioctl/TXFS_LIST_TRANSACTIONS"
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
 - TXFS_LIST_TRANSACTIONS
product: Windows
targetos: Windows
req.typenames: TXFS_LIST_TRANSACTIONS, *PTXFS_LIST_TRANSACTIONS
req.redist: 
ms.custom: 19H1
---

# TXFS_LIST_TRANSACTIONS structure


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://msdn.microsoft.com/9ee26e7e-990e-4cd3-8180-f0fcaac2b752">Alternatives to using Transactional NTFS</a>.]

Contains a list of transactions.


## -struct-fields




### -field NumberOfTransactions

The number of transactions for this resource manager.


### -field BufferSizeRequired

The length of the buffer required to hold the complete list of transactions at the time of this call. The number of transactions returned from one call to the next can change depending on the number of active transactions at any given point in time. If this call returns a request for a larger buffer, that size may or may not be adequate for the next call, based on the number of active transactions at the time of the next call.


## -see-also




<a href="https://msdn.microsoft.com/ff319bf0-2bd4-4824-bf97-b9b6eab90915">FSCTL_TXFS_LIST_TRANSACTIONS</a>



<a href="https://msdn.microsoft.com/7de14fb1-1972-4bf0-b0e2-f0344e963eef">TXFS_LIST_TRANSACTIONS_ENTRY</a>
 

 

