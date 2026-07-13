---
UID: NS:winioctl._TXFS_WRITE_BACKUP_INFORMATION
title: TXFS_WRITE_BACKUP_INFORMATION
description: Contains a Transactional NTFS (TxF) specific structure. This information should only be used when calling TXFS_WRITE_BACKUP_INFORMATION. (TXFS_WRITE_BACKUP_INFORMATION)
helpviewer_keywords: ["*PTXFS_WRITE_BACKUP_INFORMATION","PTXFS_WRITE_BACKUP_INFORMATION","PTXFS_WRITE_BACKUP_INFORMATION structure pointer [Files]","TXFS_WRITE_BACKUP_INFORMATION","TXFS_WRITE_BACKUP_INFORMATION structure [Files]","fs.txfs_write_backup_information","winioctl/PTXFS_WRITE_BACKUP_INFORMATION","winioctl/TXFS_WRITE_BACKUP_INFORMATION"]
old-location: fs\txfs_write_backup_information.htm
tech.root: fs
ms.assetid: 777210c4-4e9b-484e-a412-8c807882facb
ms.date: 12/05/2018
ms.keywords: '*PTXFS_WRITE_BACKUP_INFORMATION, PTXFS_WRITE_BACKUP_INFORMATION, PTXFS_WRITE_BACKUP_INFORMATION structure pointer [Files], TXFS_WRITE_BACKUP_INFORMATION, TXFS_WRITE_BACKUP_INFORMATION structure [Files], fs.txfs_write_backup_information, winioctl/PTXFS_WRITE_BACKUP_INFORMATION, winioctl/TXFS_WRITE_BACKUP_INFORMATION'
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
req.typenames: TXFS_WRITE_BACKUP_INFORMATION, *PTXFS_WRITE_BACKUP_INFORMATION
req.redist: 
f1_keywords:
 - _TXFS_WRITE_BACKUP_INFORMATION
 - winioctl/_TXFS_WRITE_BACKUP_INFORMATION
 - PTXFS_WRITE_BACKUP_INFORMATION
 - winioctl/PTXFS_WRITE_BACKUP_INFORMATION
 - TXFS_WRITE_BACKUP_INFORMATION
 - winioctl/TXFS_WRITE_BACKUP_INFORMATION
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
 - TXFS_WRITE_BACKUP_INFORMATION
---

# TXFS_WRITE_BACKUP_INFORMATION structure


## -description

<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Contains a Transactional NTFS (TxF) specific structure. This information should only be used when calling TXFS_WRITE_BACKUP_INFORMATION.

## -struct-fields

### -field Buffer

The buffer for the data.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_txfs_write_backup_information">FSCTL_TXFS_WRITE_BACKUP_INFORMATION</a>
