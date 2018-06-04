---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _TXFS_GET_METADATA_INFO_OUT structure


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://msdn.microsoft.com/9ee26e7e-990e-4cd3-8180-f0fcaac2b752">Alternatives to using Transactional NTFS</a>.]

Contains the version information about the miniversion that is created.


## -struct-fields




### -field TxfFileId


### -field TxfFileId.LowPart

The lower half of the TxfId of the file referenced by the handle used to call <a href="https://msdn.microsoft.com/129e682c-bc95-46d5-a0d3-adbadc7e6478">FSCTL_TXFS_GET_METADATA_INFO</a>. It is unique within a resource manager.


### -field TxfFileId.HighPart

The higher half of the TxfId of the file referenced by the handle used to call <a href="https://msdn.microsoft.com/129e682c-bc95-46d5-a0d3-adbadc7e6478">FSCTL_TXFS_GET_METADATA_INFO</a>. It is unique within a resource manager.


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




<a href="https://msdn.microsoft.com/129e682c-bc95-46d5-a0d3-adbadc7e6478">FSCTL_TXFS_GET_METADATA_INFO</a>
 

 

