---
UID: NF:msrdc.ISimilarityFileIdTable.CreateTableIndirect
title: ISimilarityFileIdTable::CreateTableIndirect
author: windows-driver-content
description: Creates or opens a similarity file ID table using the RDC application's implementation of the IRdcFileWriter interface.
old-location: rdc\isimilarityfileidtable_createtableindirect.htm
old-project: Rdc
ms.assetid: 6e472ab0-efa4-4edd-8d78-68d5a66cf41c
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: CreateTableIndirect, CreateTableIndirect method [Remote Differential Compression], CreateTableIndirect method [Remote Differential Compression],ISimilarityFileIdTable interface, ISimilarityFileIdTable interface [Remote Differential Compression],CreateTableIndirect method, ISimilarityFileIdTable.CreateTableIndirect, ISimilarityFileIdTable::CreateTableIndirect, fs.isimilarityfileidtable_createtableindirect, msrdc/ISimilarityFileIdTable::CreateTableIndirect, rdc.isimilarityfileidtable_createtableindirect
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
-	ISimilarityFileIdTable.CreateTableIndirect
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISimilarityFileIdTable::CreateTableIndirect


## -description


 Creates or opens a similarity file ID table using the RDC application's implementation of the <a href="https://msdn.microsoft.com/8b6ac8d0-37fd-4bd3-aa44-5b57f546364d">IRdcFileWriter</a> interface.


## -parameters




### -param fileIdFile [in]

An <a href="https://msdn.microsoft.com/8b6ac8d0-37fd-4bd3-aa44-5b57f546364d">IRdcFileWriter</a> interface pointer initialized to 
      write the file ID table to the file.


### -param truncate [in]

<b>TRUE</b> if a new similarity file ID table should always be created or truncated. If <b>FALSE</b> is specified and the table exists and is valid, it may be used; otherwise, if the table is not valid or does not exist, the existing table is overwritten.


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
 

 

