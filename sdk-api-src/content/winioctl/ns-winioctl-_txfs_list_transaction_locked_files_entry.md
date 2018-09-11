---
UID: NS:winioctl._TXFS_LIST_TRANSACTION_LOCKED_FILES_ENTRY
title: "_TXFS_LIST_TRANSACTION_LOCKED_FILES_ENTRY"
author: windows-sdk-content
description: Contains information about a locked transaction.
old-location: fs\txfs_list_transaction_locked_files_entry.htm
tech.root: fileio
ms.assetid: 220ccb27-c7a2-4d4e-8efd-5c8f8d1697cd
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PTXFS_LIST_TRANSACTION_LOCKED_FILES_ENTRY, PTXFS_LIST_TRANSACTION_LOCKED_FILES_ENTRY, PTXFS_LIST_TRANSACTION_LOCKED_FILES_ENTRY structure pointer [Files], TXFS_LIST_TRANSACTION_LOCKED_FILES_ENTRY, TXFS_LIST_TRANSACTION_LOCKED_FILES_ENTRY structure [Files], TXFS_LIST_TRANSACTION_LOCKED_FILES_ENTRY_FLAG_CREATED, TXFS_LIST_TRANSACTION_LOCKED_FILES_ENTRY_FLAG_DELETED, _TXFS_LIST_TRANSACTION_LOCKED_FILES_ENTRY, fs.txfs_list_transaction_locked_files_entry, winioctl/PTXFS_LIST_TRANSACTION_LOCKED_FILES_ENTRY, winioctl/TXFS_LIST_TRANSACTION_LOCKED_FILES_ENTRY"
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
 - TXFS_LIST_TRANSACTION_LOCKED_FILES_ENTRY
product: Windows
targetos: Windows
req.typenames: TXFS_LIST_TRANSACTION_LOCKED_FILES_ENTRY, *PTXFS_LIST_TRANSACTION_LOCKED_FILES_ENTRY
req.redist: 
---

# _TXFS_LIST_TRANSACTION_LOCKED_FILES_ENTRY structure


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://msdn.microsoft.com/9ee26e7e-990e-4cd3-8180-f0fcaac2b752">Alternatives to using Transactional NTFS</a>.]

Contains information about a locked transaction.


## -struct-fields




### -field Offset

The offset, in bytes, from the beginning of the 
      <a href="https://msdn.microsoft.com/55ef34c5-8d99-457d-b670-8c9efaa2eae2">TXFS_LIST_TRANSACTION_LOCKED_FILES</a> 
      structure to the next 
      <b>TXFS_LIST_TRANSACTION_LOCKED_FILES_ENTRY</b>.


### -field NameFlags

Indicates whether the current name was deleted or created in the current transaction. Note that both flags 
      may appear if the name was both created and deleted in the same transaction.  In that case, the 
      <b>FileName</b> member will contain only an empty string with a terminating null character 
      ("\0") because there is no meaningful name to report.



#### TXFS_LIST_TRANSACTION_LOCKED_FILES_ENTRY_FLAG_CREATED (0x00000001)



#### TXFS_LIST_TRANSACTION_LOCKED_FILES_ENTRY_FLAG_DELETED (0x00000002)


### -field FileId

The NTFS File ID of the file.


### -field Reserved1

Reserved. Specify zero.


### -field Reserved2

Reserved. Specify zero.


### -field Reserved3

Reserved. Specify zero.


### -field FileName

The path to the file, relative to the volume root. The file name is a NULL-terminated Unicode string.


## -see-also




<a href="https://msdn.microsoft.com/fdef45fd-b197-4428-96c5-ac91b43681b1">FSCTL_TXFS_LIST_TRANSACTION_LOCKED_FILES</a>



<a href="https://msdn.microsoft.com/55ef34c5-8d99-457d-b670-8c9efaa2eae2">TXFS_LIST_TRANSACTION_LOCKED_FILES</a>
 

 

