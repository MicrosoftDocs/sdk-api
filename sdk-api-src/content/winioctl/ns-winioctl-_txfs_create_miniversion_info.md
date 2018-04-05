---
UID: NS:winioctl._TXFS_CREATE_MINIVERSION_INFO
title: "_TXFS_CREATE_MINIVERSION_INFO"
author: windows-driver-content
description: Contains the version information about the miniversion created by FSCTL_TXFS_CREATE_MINIVERSION.
old-location: fs\txfs_create_miniversion_info.htm
old-project: FileIO
ms.assetid: 247d1471-08f4-4717-bcd8-be9d01e23d79
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: "*PTXFS_CREATE_MINIVERSION_INFO, PTXFS_CREATE_MINIVERSION_INFO, PTXFS_CREATE_MINIVERSION_INFO structure pointer [Files], TXFS_CREATE_MINIVERSION_INFO, TXFS_CREATE_MINIVERSION_INFO structure [Files], _TXFS_CREATE_MINIVERSION_INFO, fs.txfs_create_miniversion_info, winioctl/PTXFS_CREATE_MINIVERSION_INFO, winioctl/TXFS_CREATE_MINIVERSION_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: TXFS_CREATE_MINIVERSION_INFO, *PTXFS_CREATE_MINIVERSION_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoCtl.h
api_name:
-	TXFS_CREATE_MINIVERSION_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _TXFS_CREATE_MINIVERSION_INFO structure


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://msdn.microsoft.com/9ee26e7e-990e-4cd3-8180-f0fcaac2b752">Alternatives to using Transactional NTFS</a>.]

Contains the version information about the miniversion created by <a href="https://msdn.microsoft.com/3d12b149-ab34-46c4-89fc-8ddc12a81fa0">FSCTL_TXFS_CREATE_MINIVERSION</a>.


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




<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/3d12b149-ab34-46c4-89fc-8ddc12a81fa0">FSCTL_TXFS_CREATE_MINIVERSION</a>
 

 

