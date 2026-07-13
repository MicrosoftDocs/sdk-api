---
UID: NF:msrdc.ISimilarity.CreateTable
title: ISimilarity::CreateTable (msrdc.h)
description: Creates or opens a similarity traits table and a similarity file ID table.
helpviewer_keywords: ["CreateTable","CreateTable method [Remote Differential Compression]","CreateTable method [Remote Differential Compression]","ISimilarity interface","ISimilarity interface [Remote Differential Compression]","CreateTable method","ISimilarity.CreateTable","ISimilarity::CreateTable","fs.isimilarity_createtable","msrdc/ISimilarity::CreateTable","rdc.isimilarity_createtable"]
old-location: rdc\isimilarity_createtable.htm
tech.root: rdc
ms.assetid: 808c20f9-054d-475d-8ca3-ee2dde871426
ms.date: 12/05/2018
ms.keywords: CreateTable, CreateTable method [Remote Differential Compression], CreateTable method [Remote Differential Compression],ISimilarity interface, ISimilarity interface [Remote Differential Compression],CreateTable method, ISimilarity.CreateTable, ISimilarity::CreateTable, fs.isimilarity_createtable, msrdc/ISimilarity::CreateTable, rdc.isimilarity_createtable
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
 - ISimilarity::CreateTable
 - msrdc/ISimilarity::CreateTable
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
 - ISimilarity.CreateTable
---

# ISimilarity::CreateTable


## -description

Creates or opens a similarity traits table and a similarity file ID table.

## -parameters

### -param path [in]

A pointer to a null-terminated string that specifies the name of the file that will contain the tables. The similarity traits table and the similarity file ID table will be created in two alternate file streams of this file. For more information, see the <i>path</i> parameter of the <a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarityfileidtable-createtable">ISimilarityFileIdTable::CreateTable</a> and <a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilaritytraitstable-createtable">ISimilarityTraitsTable::CreateTable</a> methods.

### -param truncate [in]

<b>TRUE</b> if a new similarity traits table and a new similarity file ID table should always be created or truncated. If <b>FALSE</b> is specified and these tables exist and are valid, they may be used; otherwise, if one of the tables is not valid or does not exist, any existing tables are overwritten.

### -param securityDescriptor [in]

A pointer to a  security descriptor to use when opening the file. If this parameter is <b>NULL</b>, the file is assigned a default security descriptor. The access control lists (ACL) in the file's default security descriptor are inherited from the file's parent directory. For more information, see the <i>lpSecurityAttributes</i> parameter of the <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function.

### -param recordSize [in]

The size, in bytes, of each file ID to be stored in the similarity file id table. All similarity file IDs must be the same size. The valid range is from <b>SimilarityFileIdMinSize</b> to <b>SimilarityFileIdMaxSize</b>. If existing tables are being opened, the value of this parameter must match the file ID size of the existing similarity file ID table. Otherwise, the existing tables are assumed to be not valid and will be overwritten.

### -param isNew [out]

A pointer to  a variable that receives an  <a href="/windows/win32/api/msrdc/ne-msrdc-rdccreatedtables">RdcCreatedTables</a> enumeration value that describes the state of the tables. If new tables are created, this variable receives <b>RDCTABLE_New</b>. If existing tables are used, this variable receives <b>RDCTABLE_Existing</b>. If this method fails, this variable receives <b>RDCTABLE_InvalidOrUnknown</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If one of the tables can be created or opened successfully, but the other one cannot, both tables are marked as not valid, and the variable that the <i>isNew</i> parameter points to receives <b>RDCTABLE_InvalidOrUnknown</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilarity">ISimilarity</a>