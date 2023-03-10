---
UID: NS:winioctl._TXFS_CREATE_MINIVERSION_INFO
title: TXFS_CREATE_MINIVERSION_INFO
description: Contains the version information about the miniversion created by FSCTL_TXFS_CREATE_MINIVERSION.
helpviewer_keywords: ["*PTXFS_CREATE_MINIVERSION_INFO","PTXFS_CREATE_MINIVERSION_INFO","PTXFS_CREATE_MINIVERSION_INFO structure pointer [Files]","TXFS_CREATE_MINIVERSION_INFO","TXFS_CREATE_MINIVERSION_INFO structure [Files]","fs.txfs_create_miniversion_info","winioctl/PTXFS_CREATE_MINIVERSION_INFO","winioctl/TXFS_CREATE_MINIVERSION_INFO"]
old-location: fs\txfs_create_miniversion_info.htm
tech.root: fs
ms.assetid: 247d1471-08f4-4717-bcd8-be9d01e23d79
ms.date: 12/05/2018
ms.keywords: '*PTXFS_CREATE_MINIVERSION_INFO, PTXFS_CREATE_MINIVERSION_INFO, PTXFS_CREATE_MINIVERSION_INFO structure pointer [Files], TXFS_CREATE_MINIVERSION_INFO, TXFS_CREATE_MINIVERSION_INFO structure [Files], fs.txfs_create_miniversion_info, winioctl/PTXFS_CREATE_MINIVERSION_INFO, winioctl/TXFS_CREATE_MINIVERSION_INFO'
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
req.typenames: TXFS_CREATE_MINIVERSION_INFO, *PTXFS_CREATE_MINIVERSION_INFO
req.redist: 
f1_keywords:
 - _TXFS_CREATE_MINIVERSION_INFO
 - winioctl/_TXFS_CREATE_MINIVERSION_INFO
 - PTXFS_CREATE_MINIVERSION_INFO
 - winioctl/PTXFS_CREATE_MINIVERSION_INFO
 - TXFS_CREATE_MINIVERSION_INFO
 - winioctl/TXFS_CREATE_MINIVERSION_INFO
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
 - TXFS_CREATE_MINIVERSION_INFO
---

# TXFS_CREATE_MINIVERSION_INFO structure


## -description

<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Contains the version information about the miniversion created by <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_txfs_create_miniversion">FSCTL_TXFS_CREATE_MINIVERSION</a>.

## -struct-fields

### -field StructureVersion

The version number of this <b>TXFS_CREATE_MINIVERSION_INFO</b> structure.

### -field StructureLength

The length of this <b>TXFS_CREATE_MINIVERSION_INFO</b> structure.

### -field BaseVersion

The identifier of the most recently committed version of the file.

### -field MiniVersion

The identifier of the newly-created miniversion.

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_txfs_create_miniversion">FSCTL_TXFS_CREATE_MINIVERSION</a>