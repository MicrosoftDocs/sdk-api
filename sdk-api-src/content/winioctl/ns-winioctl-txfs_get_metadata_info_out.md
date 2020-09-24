---
UID: NS:winioctl._TXFS_GET_METADATA_INFO_OUT
title: TXFS_GET_METADATA_INFO_OUT
description: Contains the version information about the miniversion that is created.
helpviewer_keywords: ["*PTXFS_GET_METADATA_INFO_OUT","PTXFS_GET_METADATA_INFO_OUT","PTXFS_GET_METADATA_INFO_OUT structure pointer [Files]","TXFS_GET_METADATA_INFO_OUT","TXFS_GET_METADATA_INFO_OUT structure [Files]","TXFS_TRANSACTION_STATE_ACTIVE","TXFS_TRANSACTION_STATE_NONE","TXFS_TRANSACTION_STATE_NOTACTIVETXFS_TRANSACTION_STATE_NOTACTIVE","TXFS_TRANSACTION_STATE_PREPARED","fs.txfs_get_metadata_info_out","winioctl/PTXFS_GET_METADATA_INFO_OUT","winioctl/TXFS_GET_METADATA_INFO_OUT"]
old-location: fs\txfs_get_metadata_info_out.htm
tech.root: fs
ms.assetid: 138fbd75-9d2e-4969-84a7-3cebde683d93
ms.date: 12/05/2018
ms.keywords: '*PTXFS_GET_METADATA_INFO_OUT, PTXFS_GET_METADATA_INFO_OUT, PTXFS_GET_METADATA_INFO_OUT structure pointer [Files], TXFS_GET_METADATA_INFO_OUT, TXFS_GET_METADATA_INFO_OUT structure [Files], TXFS_TRANSACTION_STATE_ACTIVE, TXFS_TRANSACTION_STATE_NONE, TXFS_TRANSACTION_STATE_NOTACTIVETXFS_TRANSACTION_STATE_NOTACTIVE, TXFS_TRANSACTION_STATE_PREPARED, fs.txfs_get_metadata_info_out, winioctl/PTXFS_GET_METADATA_INFO_OUT, winioctl/TXFS_GET_METADATA_INFO_OUT'
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
req.typenames: TXFS_GET_METADATA_INFO_OUT, *PTXFS_GET_METADATA_INFO_OUT
req.redist: 
f1_keywords:
 - _TXFS_GET_METADATA_INFO_OUT
 - winioctl/_TXFS_GET_METADATA_INFO_OUT
 - PTXFS_GET_METADATA_INFO_OUT
 - winioctl/PTXFS_GET_METADATA_INFO_OUT
 - TXFS_GET_METADATA_INFO_OUT
 - winioctl/TXFS_GET_METADATA_INFO_OUT
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
 - TXFS_GET_METADATA_INFO_OUT
---

# TXFS_GET_METADATA_INFO_OUT structure


## -description

<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Contains the version information about the miniversion that is created.

## -struct-fields

### -field TxfFileId

### -field TxfFileId.LowPart

The lower half of the TxfId of the file referenced by the handle used to call <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_txfs_get_metadata_info">FSCTL_TXFS_GET_METADATA_INFO</a>. It is unique within a resource manager.

### -field TxfFileId.HighPart

The higher half of the TxfId of the file referenced by the handle used to call <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_txfs_get_metadata_info">FSCTL_TXFS_GET_METADATA_INFO</a>. It is unique within a resource manager.

### -field LockingTransaction

The <b>GUID</b> of the transaction that locked the specified file locked, if the file is locked.

### -field LastLsn

    Receives the last LSN for the most recent log record written for file. It is a property of the file that refers to the log, and references the last log entry of the file.

### -field TransactionState

Indicates the state of the transaction that has locked the file. Valid values are:

<a id="TXFS_TRANSACTION_STATE_ACTIVE"></a>
<a id="txfs_transaction_state_active"></a>


#### TXFS_TRANSACTION_STATE_ACTIVE

<a id="TXFS_TRANSACTION_STATE_NONE"></a>
<a id="txfs_transaction_state_none"></a>


#### TXFS_TRANSACTION_STATE_NONE

<a id="TXFS_TRANSACTION_STATE_NOTACTIVETXFS_TRANSACTION_STATE_NOTACTIVE"></a>
<a id="txfs_transaction_state_notactivetxfs_transaction_state_notactive"></a>


#### TXFS_TRANSACTION_STATE_NOTACTIVETXFS_TRANSACTION_STATE_NOTACTIVE

<a id="TXFS_TRANSACTION_STATE_PREPARED"></a>
<a id="txfs_transaction_state_prepared"></a>


#### TXFS_TRANSACTION_STATE_PREPARED

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_txfs_get_metadata_info">FSCTL_TXFS_GET_METADATA_INFO</a>