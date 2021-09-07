---
UID: NF:msrdc.ISimilarityFileIdTable.CreateTableIndirect
title: ISimilarityFileIdTable::CreateTableIndirect (msrdc.h)
description: Creates or opens a similarity file ID table using the RDC application's implementation of the IRdcFileWriter interface.
helpviewer_keywords: ["CreateTableIndirect","CreateTableIndirect method [Remote Differential Compression]","CreateTableIndirect method [Remote Differential Compression]","ISimilarityFileIdTable interface","ISimilarityFileIdTable interface [Remote Differential Compression]","CreateTableIndirect method","ISimilarityFileIdTable.CreateTableIndirect","ISimilarityFileIdTable::CreateTableIndirect","fs.isimilarityfileidtable_createtableindirect","msrdc/ISimilarityFileIdTable::CreateTableIndirect","rdc.isimilarityfileidtable_createtableindirect"]
old-location: rdc\isimilarityfileidtable_createtableindirect.htm
tech.root: rdc
ms.assetid: 6e472ab0-efa4-4edd-8d78-68d5a66cf41c
ms.date: 12/05/2018
ms.keywords: CreateTableIndirect, CreateTableIndirect method [Remote Differential Compression], CreateTableIndirect method [Remote Differential Compression],ISimilarityFileIdTable interface, ISimilarityFileIdTable interface [Remote Differential Compression],CreateTableIndirect method, ISimilarityFileIdTable.CreateTableIndirect, ISimilarityFileIdTable::CreateTableIndirect, fs.isimilarityfileidtable_createtableindirect, msrdc/ISimilarityFileIdTable::CreateTableIndirect, rdc.isimilarityfileidtable_createtableindirect
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
 - ISimilarityFileIdTable::CreateTableIndirect
 - msrdc/ISimilarityFileIdTable::CreateTableIndirect
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
 - ISimilarityFileIdTable.CreateTableIndirect
---

# ISimilarityFileIdTable::CreateTableIndirect


## -description

 Creates or opens a similarity file ID table using the RDC application's implementation of the <a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcfilewriter">IRdcFileWriter</a> interface.

## -parameters

### -param fileIdFile [in]

An <a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcfilewriter">IRdcFileWriter</a> interface pointer initialized to 
      write the file ID table to the file.

### -param truncate [in]

<b>TRUE</b> if a new similarity file ID table should always be created or truncated. If <b>FALSE</b> is specified and the table exists and is valid, it may be used; otherwise, if the table is not valid or does not exist, the existing table is overwritten.

### -param recordSize [in]

The size, in bytes, of the file IDs that will be stored in the similarity file ID table. All file IDs must be the same size. The valid range is from <b>SimilarityFileIdMinSize</b> to <b>SimilarityFileIdMaxSize</b>. If an existing similarity file ID table is being opened, the value of this parameter must match the file ID size of the existing table. Otherwise, the existing table is assumed to be not valid and will be overwritten.

### -param isNew [out]

A pointer to a variable that receives an  <a href="/windows/win32/api/msrdc/ne-msrdc-rdccreatedtables">RdcCreatedTables</a> enumeration value that describes the state of the similarity file ID table. If a new table is created, this variable receives <b>RDCTABLE_New</b>. If an existing table is used, this variable receives <b>RDCTABLE_Existing</b>. If this method fails, this variable receives <b>RDCTABLE_InvalidOrUnknown</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If an existing table is being opened, the table must be valid, and the value of the <i>recordSize</i> parameter must match  the record size of the existing table.  Otherwise, the existing table is overwritten, even if <b>FALSE</b> is specified for the <i>truncate</i> parameter.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilarityfileidtable">ISimilarityFileIdTable</a>