---
UID: NS:winioctl._TXFS_TRANSACTION_ACTIVE_INFO
title: TXFS_TRANSACTION_ACTIVE_INFO
description: Contains the flag that indicates whether transactions were active or not when a snapshot was taken.
helpviewer_keywords: ["*PTXFS_TRANSACTION_ACTIVE_INFO","PTXFS_TRANSACTION_ACTIVE_INFO","PTXFS_TRANSACTION_ACTIVE_INFO structure pointer [Files]","TXFS_TRANSACTION_ACTIVE_INFO","TXFS_TRANSACTION_ACTIVE_INFO structure [Files]","fs.txfs_transaction_active_info","winioctl/PTXFS_TRANSACTION_ACTIVE_INFO","winioctl/TXFS_TRANSACTION_ACTIVE_INFO"]
old-location: fs\txfs_transaction_active_info.htm
tech.root: fs
ms.assetid: 72ab7652-7841-4195-a109-1caf65b629f1
ms.date: 12/05/2018
ms.keywords: '*PTXFS_TRANSACTION_ACTIVE_INFO, PTXFS_TRANSACTION_ACTIVE_INFO, PTXFS_TRANSACTION_ACTIVE_INFO structure pointer [Files], TXFS_TRANSACTION_ACTIVE_INFO, TXFS_TRANSACTION_ACTIVE_INFO structure [Files], fs.txfs_transaction_active_info, winioctl/PTXFS_TRANSACTION_ACTIVE_INFO, winioctl/TXFS_TRANSACTION_ACTIVE_INFO'
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
req.typenames: TXFS_TRANSACTION_ACTIVE_INFO, *PTXFS_TRANSACTION_ACTIVE_INFO
req.redist: 
f1_keywords:
 - _TXFS_TRANSACTION_ACTIVE_INFO
 - winioctl/_TXFS_TRANSACTION_ACTIVE_INFO
 - PTXFS_TRANSACTION_ACTIVE_INFO
 - winioctl/PTXFS_TRANSACTION_ACTIVE_INFO
 - TXFS_TRANSACTION_ACTIVE_INFO
 - winioctl/TXFS_TRANSACTION_ACTIVE_INFO
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
 - TXFS_TRANSACTION_ACTIVE_INFO
---

# TXFS_TRANSACTION_ACTIVE_INFO structure


## -description

<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Contains the flag that indicates whether transactions were active or not when a snapshot was taken.

## -struct-fields

### -field TransactionsActiveAtSnapshot

This member is <b>TRUE</b> if the mounted snapshot volume had active transactions when the snapshot was taken; and <b>FALSE</b> otherwise.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_txfs_transaction_active">FSCTL_TXFS_TRANSACTION_ACTIVE</a>