---
UID: NE:imapi2fs.FsiItemType
title: FsiItemType
author: windows-sdk-content
description: Defines values for the file system item that was found using the IFileSystemImage::Exists method.
old-location: imapi\fsiitemtype.htm
tech.root: imapi
ms.assetid: b0ddf0fc-30db-464d-8761-da400386a609
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FsiItemDirectory, FsiItemFile, FsiItemNotFound, FsiItemType, FsiItemType enumeration [IMAPI], imapi.fsiitemtype, imapi2fs/FsiItemDirectory, imapi2fs/FsiItemFile, imapi2fs/FsiItemNotFound, imapi2fs/FsiItemType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2fs.idl
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
 - imapi2fs.h
api_name:
 - FsiItemType
product: Windows
targetos: Windows
req.typenames: FsiItemType
req.redist: 
---

# FsiItemType enumeration


## -description


Defines values for the file system item that was found using the <a href="https://msdn.microsoft.com/c3a86e85-1ffd-47c1-9dba-0fc207d76a1a">IFileSystemImage::Exists</a> method.


## -enum-fields




### -field FsiItemNotFound

The specified item was not found.


### -field FsiItemDirectory

The specified item is a directory.


### -field FsiItemFile

The specified item is a file.


## -see-also




<a href="https://msdn.microsoft.com/c3a86e85-1ffd-47c1-9dba-0fc207d76a1a">IFileSystemImage::Exists</a>
 

 

