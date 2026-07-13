---
UID: NF:msrdc.ISimilarityTraitsTable.CreateTable
title: ISimilarityTraitsTable::CreateTable (msrdc.h)
description: Creates or opens a similarity traits table.
helpviewer_keywords: ["CreateTable","CreateTable method [Remote Differential Compression]","CreateTable method [Remote Differential Compression]","ISimilarityTraitsTable interface","ISimilarityTraitsTable interface [Remote Differential Compression]","CreateTable method","ISimilarityTraitsTable.CreateTable","ISimilarityTraitsTable::CreateTable","fs.isimilaritytraitstable_createtable","msrdc/ISimilarityTraitsTable::CreateTable","rdc.isimilaritytraitstable_createtable"]
old-location: rdc\isimilaritytraitstable_createtable.htm
tech.root: rdc
ms.assetid: 35fd9ea1-85bf-424c-b0e2-dcdfbb6940fb
ms.date: 12/05/2018
ms.keywords: CreateTable, CreateTable method [Remote Differential Compression], CreateTable method [Remote Differential Compression],ISimilarityTraitsTable interface, ISimilarityTraitsTable interface [Remote Differential Compression],CreateTable method, ISimilarityTraitsTable.CreateTable, ISimilarityTraitsTable::CreateTable, fs.isimilaritytraitstable_createtable, msrdc/ISimilarityTraitsTable::CreateTable, rdc.isimilaritytraitstable_createtable
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
req.lib: 
req.dll: MsRdc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISimilarityTraitsTable::CreateTable
 - msrdc/ISimilarityTraitsTable::CreateTable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - ISimilarityTraitsTable.CreateTable
---

# ISimilarityTraitsTable::CreateTable


## -description

Creates or opens a similarity traits table.

## -parameters

### -param path [in]

A pointer to a null-terminated string that specifies the name of the file that will contain the similarity traits table. The alternate stream name ":Traits" will be appended to the end of this file name. For more information, see <a href="/windows/desktop/FileIO/naming-a-file">Naming a File</a>.

### -param truncate [in]

<b>TRUE</b> if a new similarity traits table should always be created or truncated. If <b>FALSE</b> is specified and the table exists and is valid, it may be used; otherwise, if the table is not valid or does not exist, the existing table is overwritten.

### -param securityDescriptor [in]

A pointer to a  security descriptor to use when opening the file. If this parameter is <b>NULL</b>, the file is assigned a default security descriptor. The access control lists (ACL) in the file's default security descriptor are inherited from the file's parent directory. For more information, see the <i>lpSecurityAttributes</i> parameter of the <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function.

### -param isNew [out]

A pointer to a variable that receives an  <a href="/windows/win32/api/msrdc/ne-msrdc-rdccreatedtables">RdcCreatedTables</a> enumeration value that describes the state of the similarity traits table. If a new table is created, this variable receives <b>RDCTABLE_New</b>. If an existing table is used, this variable receives <b>RDCTABLE_Existing</b>. If this method fails, this variable receives <b>RDCTABLE_InvalidOrUnknown</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If an existing similarity traits table is being opened, the table must be valid.  Otherwise, the existing table is overwritten, even if <b>FALSE</b> is specified for the <i>truncate</i> parameter.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilaritytraitstable">ISimilarityTraitsTable</a>