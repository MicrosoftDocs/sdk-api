---
UID: NS:winioctl._TXFS_WRITE_BACKUP_INFORMATION
title: "_TXFS_WRITE_BACKUP_INFORMATION"
author: windows-sdk-content
description: Contains a Transactional NTFS (TxF) specific structure. This information should only be used when calling TXFS_WRITE_BACKUP_INFORMATION.
old-location: fs\txfs_write_backup_information.htm
tech.root: fileio
ms.assetid: 777210c4-4e9b-484e-a412-8c807882facb
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: "*PTXFS_WRITE_BACKUP_INFORMATION, PTXFS_WRITE_BACKUP_INFORMATION, PTXFS_WRITE_BACKUP_INFORMATION structure pointer [Files], TXFS_WRITE_BACKUP_INFORMATION, TXFS_WRITE_BACKUP_INFORMATION structure [Files], _TXFS_WRITE_BACKUP_INFORMATION, fs.txfs_write_backup_information, winioctl/PTXFS_WRITE_BACKUP_INFORMATION, winioctl/TXFS_WRITE_BACKUP_INFORMATION"
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
 - TXFS_WRITE_BACKUP_INFORMATION
product: Windows
targetos: Windows
req.typenames: TXFS_WRITE_BACKUP_INFORMATION, *PTXFS_WRITE_BACKUP_INFORMATION
req.redist: 
---

# _TXFS_WRITE_BACKUP_INFORMATION structure


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://msdn.microsoft.com/9ee26e7e-990e-4cd3-8180-f0fcaac2b752">Alternatives to using Transactional NTFS</a>.]

Contains a Transactional NTFS (TxF) specific structure. This information should only be used when calling <a href="https://msdn.microsoft.com/c2b9ce2f-9f08-4706-9565-423ab0dc493f">TXFS_WRITE_BACKUP_INFORMATION</a>.


## -struct-fields




### -field Buffer

The buffer for the data.


## -see-also




<a href="https://msdn.microsoft.com/36080d53-9004-40f7-9d92-c6deaac8299f">FSCTL_TXFS_WRITE_BACKUP_INFORMATION</a>
 

 

