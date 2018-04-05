---
UID: NE:winbase._FILE_ID_TYPE
title: "_FILE_ID_TYPE"
author: windows-driver-content
description: Discriminator for the union in the FILE_ID_DESCRIPTOR structure.
old-location: fs\file_id_type.htm
old-project: FileIO
ms.assetid: 7e46ba94-e3cd-4d6c-962f-5d5bd55d45a1
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: "*PFILE_ID_TYPE, ExtendedFileIdType, FILE_ID_TYPE, FILE_ID_TYPE enumeration [Files], FileIdType, MaximumFileIdType, ObjectIdType, PFILE_ID_TYPE, PFILE_ID_TYPE enumeration pointer [Files], _FILE_ID_TYPE, fileextd/ExtendedFileIdType, fileextd/FILE_ID_TYPE, fileextd/FileIdType, fileextd/MaximumFileIdType, fileextd/ObjectIdType, fileextd/PFILE_ID_TYPE, fs.file_id_type, winbase/ExtendedFileIdType, winbase/FILE_ID_TYPE, winbase/FileIdType, winbase/MaximumFileIdType, winbase/ObjectIdType, winbase/PFILE_ID_TYPE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: winbase.h
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
req.typenames: FILE_ID_TYPE, *PFILE_ID_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinBase.h
-	FileExtd.h
api_name:
-	FILE_ID_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _FILE_ID_TYPE enumeration


## -description


Discriminator for the union in the 
    <a href="https://msdn.microsoft.com/9092a701-3b47-4c4c-8221-54fa3220d322">FILE_ID_DESCRIPTOR</a> structure.


## -enum-fields




### -field FileIdType

Use the <b>FileId</b> member of the union.


### -field ObjectIdType

Use the <b>ObjectId</b> member of the union.


### -field ExtendedFileIdType

Use the <b>ExtendedFileId</b> member of the union.
      

<b>Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008, Windows 7 and Windows Server 2008 R2:  </b>This value is not supported before Windows 8 and Windows Server 2012.


### -field MaximumFileIdType

This value is used for comparison only. All valid values are less than this value.


## -see-also




<a href="https://msdn.microsoft.com/9092a701-3b47-4c4c-8221-54fa3220d322">FILE_ID_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/14b1cfff-5e47-4309-8e62-fb5c8da9ce97">File Management Enumerations</a>



<a href="https://msdn.microsoft.com/caa757a2-fc3f-4883-8d3e-b98d28f92517">OpenFileById</a>
 

 

