---
UID: NF:msrdc.ISimilarityFileIdTable.CreateTable
title: ISimilarityFileIdTable::CreateTable
author: windows-driver-content
description: Creates or opens a similarity file ID table.
old-location: rdc\isimilarityfileidtable_createtable.htm
old-project: Rdc
ms.assetid: bc683c53-5491-4cc6-abe1-c82e69aaa7f4
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: CreateTable, CreateTable method [Remote Differential Compression], CreateTable method [Remote Differential Compression],ISimilarityFileIdTable interface, ISimilarityFileIdTable interface [Remote Differential Compression],CreateTable method, ISimilarityFileIdTable.CreateTable, ISimilarityFileIdTable::CreateTable, fs.isimilarityfileidtable_createtable, msrdc/ISimilarityFileIdTable::CreateTable, rdc.isimilarityfileidtable_createtable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msrdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsRdc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RdcMappingAccessMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	MsRdc.dll
api_name:
-	ISimilarityFileIdTable.CreateTable
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISimilarityFileIdTable::CreateTable


## -description


 Creates or opens a similarity file ID table.


## -parameters




### -param path [in]

A pointer to a null-terminated string that specifies the name of the file that will contain the similarity file ID table. The alternate stream name ":FileId" will be appended to the end of this file name. For more information, see <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming a File</a>.


### -param truncate [in]

<b>TRUE</b> if a new similarity file ID table should always be created or truncated. If <b>FALSE</b> is specified and the table exists and is valid, it may be used; otherwise, if the table is not valid or does not exist, the existing table is overwritten.


### -param securityDescriptor [in]

A pointer to a  security descriptor to use when opening the file. If this parameter is <b>NULL</b>, the file is assigned a default security descriptor. The access control lists (ACL) in the file's default security descriptor are inherited from the file's parent directory. For more information, see the <i>lpSecurityAttributes</i> parameter of the <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function.


### -param recordSize [in]

The size, in bytes, of the file IDs that will be stored in the similarity file ID table. All file IDs must be the same size. The valid range is from <b>SimilarityFileIdMinSize</b> to <b>SimilarityFileIdMaxSize</b>. If an existing similarity file ID table is being opened, the value of this parameter must match the file ID size of the existing table. Otherwise, the existing table is assumed to be not valid and will be overwritten.


### -param isNew [out]

A pointer to a variable that receives an  <a href="https://msdn.microsoft.com/f46dd0f0-22b0-41fb-a7c2-29d1b4514f7e">RdcCreatedTables</a> enumeration value that describes the state of the similarity file ID table. If a new table is created, this variable receives <b>RDCTABLE_New</b>. If an existing table is used, this variable receives <b>RDCTABLE_Existing</b>. If this method fails, this variable receives <b>RDCTABLE_InvalidOrUnknown</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If an existing table is being opened, the table must be valid, and the value of the <i>recordSize</i> parameter must match  the record size of the existing table.  Otherwise, the existing table is overwritten, even if <b>FALSE</b> is specified for the <i>truncate</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/539a2e9b-9719-4012-bb7f-4d14723a3695">ISimilarityFileIdTable</a>
 

 

