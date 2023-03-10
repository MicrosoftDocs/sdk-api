---
UID: NS:winioctl._TXFS_READ_BACKUP_INFORMATION_OUT
title: TXFS_READ_BACKUP_INFORMATION_OUT
description: Contains a Transactional NTFS (TxF) specific structure. This information should only be used when calling TXFS_WRITE_BACKUP_INFORMATION. (TXFS_READ_BACKUP_INFORMATION_OUT)
helpviewer_keywords: ["*PTXFS_READ_BACKUP_INFORMATION_OUT","PTXFS_READ_BACKUP_INFORMATION_OUT","PTXFS_READ_BACKUP_INFORMATION_OUT structure pointer [Files]","TXFS_READ_BACKUP_INFORMATION_OUT","TXFS_READ_BACKUP_INFORMATION_OUT structure [Files]","fs.txfs_read_backup_information_out","winioctl/PTXFS_READ_BACKUP_INFORMATION_OUT","winioctl/TXFS_READ_BACKUP_INFORMATION_OUT"]
old-location: fs\txfs_read_backup_information_out.htm
tech.root: fs
ms.assetid: c2b9ce2f-9f08-4706-9565-423ab0dc493f
ms.date: 12/05/2018
ms.keywords: '*PTXFS_READ_BACKUP_INFORMATION_OUT, PTXFS_READ_BACKUP_INFORMATION_OUT, PTXFS_READ_BACKUP_INFORMATION_OUT structure pointer [Files], TXFS_READ_BACKUP_INFORMATION_OUT, TXFS_READ_BACKUP_INFORMATION_OUT structure [Files], fs.txfs_read_backup_information_out, winioctl/PTXFS_READ_BACKUP_INFORMATION_OUT, winioctl/TXFS_READ_BACKUP_INFORMATION_OUT'
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
req.typenames: TXFS_READ_BACKUP_INFORMATION_OUT, *PTXFS_READ_BACKUP_INFORMATION_OUT
req.redist: 
f1_keywords:
 - _TXFS_READ_BACKUP_INFORMATION_OUT
 - winioctl/_TXFS_READ_BACKUP_INFORMATION_OUT
 - PTXFS_READ_BACKUP_INFORMATION_OUT
 - winioctl/PTXFS_READ_BACKUP_INFORMATION_OUT
 - TXFS_READ_BACKUP_INFORMATION_OUT
 - winioctl/TXFS_READ_BACKUP_INFORMATION_OUT
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
 - TXFS_READ_BACKUP_INFORMATION_OUT
---

# TXFS_READ_BACKUP_INFORMATION_OUT structure


## -description

<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Contains a Transactional NTFS (TxF) specific structure. This information should only be used when 
   calling 
   <a href="/windows/desktop/api/winioctl/ns-winioctl-txfs_write_backup_information">TXFS_WRITE_BACKUP_INFORMATION</a>.

## -struct-fields

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.BufferLength

If the buffer is not large enough, this member receives the required buffer size.

### -field DUMMYUNIONNAME.Buffer

The buffer for the data.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_txfs_read_backup_information">FSCTL_TXFS_READ_BACKUP_INFORMATION</a>
