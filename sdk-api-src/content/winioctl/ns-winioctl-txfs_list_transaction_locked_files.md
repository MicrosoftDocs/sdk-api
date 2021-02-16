---
UID: NS:winioctl._TXFS_LIST_TRANSACTION_LOCKED_FILES
title: TXFS_LIST_TRANSACTION_LOCKED_FILES
description: Contains a list of files locked by a transacted writer.
helpviewer_keywords: ["*PTXFS_LIST_TRANSACTION_LOCKED_FILES","PTXFS_LIST_TRANSACTION_LOCKED_FILES","PTXFS_LIST_TRANSACTION_LOCKED_FILES structure pointer [Files]","TXFS_LIST_TRANSACTION_LOCKED_FILES","TXFS_LIST_TRANSACTION_LOCKED_FILES structure [Files]","fs.txfs_list_transaction_locked_files","winioctl/PTXFS_LIST_TRANSACTION_LOCKED_FILES","winioctl/TXFS_LIST_TRANSACTION_LOCKED_FILES"]
old-location: fs\txfs_list_transaction_locked_files.htm
tech.root: fs
ms.assetid: 55ef34c5-8d99-457d-b670-8c9efaa2eae2
ms.date: 12/05/2018
ms.keywords: '*PTXFS_LIST_TRANSACTION_LOCKED_FILES, PTXFS_LIST_TRANSACTION_LOCKED_FILES, PTXFS_LIST_TRANSACTION_LOCKED_FILES structure pointer [Files], TXFS_LIST_TRANSACTION_LOCKED_FILES, TXFS_LIST_TRANSACTION_LOCKED_FILES structure [Files], fs.txfs_list_transaction_locked_files, winioctl/PTXFS_LIST_TRANSACTION_LOCKED_FILES, winioctl/TXFS_LIST_TRANSACTION_LOCKED_FILES'
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
req.typenames: TXFS_LIST_TRANSACTION_LOCKED_FILES, *PTXFS_LIST_TRANSACTION_LOCKED_FILES
req.redist: 
f1_keywords:
 - _TXFS_LIST_TRANSACTION_LOCKED_FILES
 - winioctl/_TXFS_LIST_TRANSACTION_LOCKED_FILES
 - PTXFS_LIST_TRANSACTION_LOCKED_FILES
 - winioctl/PTXFS_LIST_TRANSACTION_LOCKED_FILES
 - TXFS_LIST_TRANSACTION_LOCKED_FILES
 - winioctl/TXFS_LIST_TRANSACTION_LOCKED_FILES
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
 - TXFS_LIST_TRANSACTION_LOCKED_FILES
---

# TXFS_LIST_TRANSACTION_LOCKED_FILES structure


## -description

<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Contains a list of files locked by a transacted writer.

## -struct-fields

### -field KtmTransaction

The KTM transaction to enumerate locked files for in this RM.

### -field NumberOfFiles

The number of files involved for the specified transaction on this resource manager.

### -field BufferSizeRequired

The length of the buffer required to hold the complete list of files at the time of this call. This is not guaranteed to be the same length as any other subsequent call.

### -field Offset

The offset from the beginning of this structure to the beginning of the first <a href="/windows/win32/api/winioctl/ns-winioctl-txfs_list_transaction_locked_files_entry">TXFS_LIST_TRANSACTION_LOCKED_FILES_ENTRY</a> structure.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_txfs_list_transaction_locked_files">FSCTL_TXFS_LIST_TRANSACTION_LOCKED_FILES</a>



<a href="/windows/win32/api/winioctl/ns-winioctl-txfs_list_transaction_locked_files_entry">TXFS_LIST_TRANSACTION_LOCKED_FILES_ENTRY</a>