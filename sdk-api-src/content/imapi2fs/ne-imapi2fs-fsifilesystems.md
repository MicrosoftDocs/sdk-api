---
UID: NE:imapi2fs.FsiFileSystems
title: FsiFileSystems
author: windows-sdk-content
description: Defines values for recognized file systems.
old-location: imapi\fsifilesystems.htm
old-project: imapi
ms.assetid: afb27235-a9b4-4629-aac0-9c43e5b2cf3f
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: FsiFileSystemISO9660, FsiFileSystemJoliet, FsiFileSystemNone, FsiFileSystemUDF, FsiFileSystemUnknown, FsiFileSystems, FsiFileSystems enumeration [IMAPI], imapi.fsifilesystems, imapi2fs/FsiFileSystemISO9660, imapi2fs/FsiFileSystemJoliet, imapi2fs/FsiFileSystemNone, imapi2fs/FsiFileSystemUDF, imapi2fs/FsiFileSystemUnknown, imapi2fs/FsiFileSystems
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: FsiFileSystems
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	imapi2fs.h
api_name:
-	FsiFileSystems
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# FsiFileSystems enumeration


## -description


Defines values for recognized file systems.


## -enum-fields




### -field FsiFileSystemNone

The disc does not contain a recognized file system.


### -field FsiFileSystemISO9660

Standard CD file system.


### -field FsiFileSystemJoliet

Joliet file system.


### -field FsiFileSystemUDF

UDF file system.


### -field FsiFileSystemUnknown

The disc appears to have a file system, but the layout does not match any of the recognized types.


## -see-also




<a href="https://msdn.microsoft.com/381be283-c877-44f0-9d96-b9e80a6aeec8">IFileSystemImage::IdentifyFileSystemsOnDisc</a>
 

 

