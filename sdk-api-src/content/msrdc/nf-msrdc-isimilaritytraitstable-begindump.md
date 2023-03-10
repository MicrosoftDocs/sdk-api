---
UID: NF:msrdc.ISimilarityTraitsTable.BeginDump
title: ISimilarityTraitsTable::BeginDump (msrdc.h)
description: Retrieves similarity data from the similarity traits table.
helpviewer_keywords: ["BeginDump","BeginDump method [Remote Differential Compression]","BeginDump method [Remote Differential Compression]","ISimilarityTraitsTable interface","ISimilarityTraitsTable interface [Remote Differential Compression]","BeginDump method","ISimilarityTraitsTable.BeginDump","ISimilarityTraitsTable::BeginDump","fs.isimilaritytraitstable_begindump","msrdc/ISimilarityTraitsTable::BeginDump","rdc.isimilaritytraitstable_begindump"]
old-location: rdc\isimilaritytraitstable_begindump.htm
tech.root: rdc
ms.assetid: 93298019-334b-4685-b95e-a1081c2bd9dc
ms.date: 12/05/2018
ms.keywords: BeginDump, BeginDump method [Remote Differential Compression], BeginDump method [Remote Differential Compression],ISimilarityTraitsTable interface, ISimilarityTraitsTable interface [Remote Differential Compression],BeginDump method, ISimilarityTraitsTable.BeginDump, ISimilarityTraitsTable::BeginDump, fs.isimilaritytraitstable_begindump, msrdc/ISimilarityTraitsTable::BeginDump, rdc.isimilaritytraitstable_begindump
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
 - ISimilarityTraitsTable::BeginDump
 - msrdc/ISimilarityTraitsTable::BeginDump
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
 - ISimilarityTraitsTable.BeginDump
---

# ISimilarityTraitsTable::BeginDump


## -description

Retrieves similarity data from the similarity traits table.

## -parameters

### -param similarityTableDumpState [out, optional]

An optional pointer to a location that will receive the returned <a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilaritytabledumpstate">ISimilarityTableDumpState</a> interface pointer. The caller must release this interface when it is no longer needed.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>BeginDump</b> method is used for debugging and garbage collection. It returns an interface pointer to an iterator object that allows the application to efficiently dump all of the entries in the similarity traits table.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilaritytraitstable">ISimilarityTraitsTable</a>