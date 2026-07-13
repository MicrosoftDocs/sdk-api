---
UID: NF:msrdc.ISimilarity.CreateTableIndirect
title: ISimilarity::CreateTableIndirect (msrdc.h)
description: Creates or opens a similarity traits table and a similarity file ID table using the RDC application's implementations of the ISimilarityTraitsMapping and IRdcFileWriter interfaces.
helpviewer_keywords: ["CreateTableIndirect","CreateTableIndirect method [Remote Differential Compression]","CreateTableIndirect method [Remote Differential Compression]","ISimilarity interface","ISimilarity interface [Remote Differential Compression]","CreateTableIndirect method","ISimilarity.CreateTableIndirect","ISimilarity::CreateTableIndirect","fs.isimilarity_createtableindirect","msrdc/ISimilarity::CreateTableIndirect","rdc.isimilarity_createtableindirect"]
old-location: rdc\isimilarity_createtableindirect.htm
tech.root: rdc
ms.assetid: 84df73f5-0c39-44bd-81d8-d5ca144eb2e8
ms.date: 12/05/2018
ms.keywords: CreateTableIndirect, CreateTableIndirect method [Remote Differential Compression], CreateTableIndirect method [Remote Differential Compression],ISimilarity interface, ISimilarity interface [Remote Differential Compression],CreateTableIndirect method, ISimilarity.CreateTableIndirect, ISimilarity::CreateTableIndirect, fs.isimilarity_createtableindirect, msrdc/ISimilarity::CreateTableIndirect, rdc.isimilarity_createtableindirect
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
 - ISimilarity::CreateTableIndirect
 - msrdc/ISimilarity::CreateTableIndirect
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
 - ISimilarity.CreateTableIndirect
---

# ISimilarity::CreateTableIndirect


## -description

Creates or opens a similarity traits table and a similarity file ID table using the RDC application's implementations of the <a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilaritytraitsmapping">ISimilarityTraitsMapping</a> and <a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcfilewriter">IRdcFileWriter</a> interfaces.

## -parameters

### -param mapping [in]

An <a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilaritytraitsmapping">ISimilarityTraitsMapping</a> interface pointer initialized to write the similarity traits table to the file.

### -param fileIdFile [in]

An <a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcfilewriter">IRdcFileWriter</a> interface pointer initialized to 
      write the file ID table to the file.

### -param truncate [in]

<b>TRUE</b> if a new similarity traits table and a new similarity file ID table should always be created or truncated. If <b>FALSE</b> is specified and these tables exist and are valid, they may be used; otherwise, if one of the tables is not valid or does not exist, any existing tables are overwritten.

### -param recordSize [in]

The size, in bytes, of each file ID to be stored in the similarity file ID table. All similarity file IDs must be the same size. The valid range is from <b>SimilarityFileIdMinSize</b> to <b>SimilarityFileIdMaxSize</b>. If existing tables are being opened, the value of this parameter must match the file ID size of the existing similarity file ID table. Otherwise, the existing tables are assumed to be not valid and will be overwritten.

### -param isNew [out]

A pointer to  a variable that receives an  <a href="/windows/win32/api/msrdc/ne-msrdc-rdccreatedtables">RdcCreatedTables</a> enumeration value that describes the state of the tables. If new tables are created, this variable receives <b>RDCTABLE_New</b>. If existing tables are used, this variable receives <b>RDCTABLE_Existing</b>. If this method fails, this variable receives <b>RDCTABLE_InvalidOrUnknown</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If one of the tables can be created or opened successfully, but the other one cannot, both tables are marked as not valid, and the variable that the <i>isNew</i> parameter points to receives <b>RDCTABLE_InvalidOrUnknown</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilarity">ISimilarity</a>