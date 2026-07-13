---
UID: NF:msrdc.ISimilarityTraitsTable.CreateTableIndirect
title: ISimilarityTraitsTable::CreateTableIndirect (msrdc.h)
description: Creates or opens a similarity traits table using the RDC application's implementation of the ISimilarityTraitsMapping interface.
helpviewer_keywords: ["CreateTableIndirect","CreateTableIndirect method [Remote Differential Compression]","CreateTableIndirect method [Remote Differential Compression]","ISimilarityTraitsTable interface","ISimilarityTraitsTable interface [Remote Differential Compression]","CreateTableIndirect method","ISimilarityTraitsTable.CreateTableIndirect","ISimilarityTraitsTable::CreateTableIndirect","fs.isimilaritytraitstable_createtableindirect","msrdc/ISimilarityTraitsTable::CreateTableIndirect","rdc.isimilaritytraitstable_createtableindirect"]
old-location: rdc\isimilaritytraitstable_createtableindirect.htm
tech.root: rdc
ms.assetid: 55bd485f-33f7-4247-bc13-f5e2c7e70028
ms.date: 12/05/2018
ms.keywords: CreateTableIndirect, CreateTableIndirect method [Remote Differential Compression], CreateTableIndirect method [Remote Differential Compression],ISimilarityTraitsTable interface, ISimilarityTraitsTable interface [Remote Differential Compression],CreateTableIndirect method, ISimilarityTraitsTable.CreateTableIndirect, ISimilarityTraitsTable::CreateTableIndirect, fs.isimilaritytraitstable_createtableindirect, msrdc/ISimilarityTraitsTable::CreateTableIndirect, rdc.isimilaritytraitstable_createtableindirect
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
 - ISimilarityTraitsTable::CreateTableIndirect
 - msrdc/ISimilarityTraitsTable::CreateTableIndirect
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
 - ISimilarityTraitsTable.CreateTableIndirect
---

# ISimilarityTraitsTable::CreateTableIndirect


## -description

Creates or opens a similarity traits table using the RDC application's implementation of the <a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilaritytraitsmapping">ISimilarityTraitsMapping</a> interface.

## -parameters

### -param mapping [in]

An <a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilaritytraitsmapping">ISimilarityTraitsMapping</a> interface pointer initialized to write the similarity traits table to the file.

### -param truncate [in]

<b>TRUE</b> if a new similarity traits table should always be created or truncated. If <b>FALSE</b> is specified and the table exists and is valid, it may be used; otherwise, if the table is not valid or does not exist, the existing table is overwritten.

### -param isNew [out]

A pointer to a variable that receives an  <a href="/windows/win32/api/msrdc/ne-msrdc-rdccreatedtables">RdcCreatedTables</a> enumeration value that describes the state of the similarity traits table. If a new table is created, this variable receives <b>RDCTABLE_New</b>. If an existing table is used, this variable receives <b>RDCTABLE_Existing</b>. If this method fails, this variable receives <b>RDCTABLE_InvalidOrUnknown</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If an existing similarity traits table is being opened, the table must be valid.  Otherwise, the existing table is overwritten, even if <b>FALSE</b> is specified for the <i>truncate</i> parameter.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilaritytraitstable">ISimilarityTraitsTable</a>