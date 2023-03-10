---
UID: NF:msrdc.ISimilarityFileIdTable.GetRecordCount
title: ISimilarityFileIdTable::GetRecordCount (msrdc.h)
description: Retrieves the number of records that are stored in a similarity file ID table.
helpviewer_keywords: ["GetRecordCount","GetRecordCount method [Remote Differential Compression]","GetRecordCount method [Remote Differential Compression]","ISimilarityFileIdTable interface","ISimilarityFileIdTable interface [Remote Differential Compression]","GetRecordCount method","ISimilarityFileIdTable.GetRecordCount","ISimilarityFileIdTable::GetRecordCount","fs.isimilarityfileidtable_getrecordcount","msrdc/ISimilarityFileIdTable::GetRecordCount","rdc.isimilarityfileidtable_getrecordcount"]
old-location: rdc\isimilarityfileidtable_getrecordcount.htm
tech.root: rdc
ms.assetid: 2d95140e-c422-4aa5-aea2-ee777f977c17
ms.date: 12/05/2018
ms.keywords: GetRecordCount, GetRecordCount method [Remote Differential Compression], GetRecordCount method [Remote Differential Compression],ISimilarityFileIdTable interface, ISimilarityFileIdTable interface [Remote Differential Compression],GetRecordCount method, ISimilarityFileIdTable.GetRecordCount, ISimilarityFileIdTable::GetRecordCount, fs.isimilarityfileidtable_getrecordcount, msrdc/ISimilarityFileIdTable::GetRecordCount, rdc.isimilarityfileidtable_getrecordcount
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
 - ISimilarityFileIdTable::GetRecordCount
 - msrdc/ISimilarityFileIdTable::GetRecordCount
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
 - ISimilarityFileIdTable.GetRecordCount
---

# ISimilarityFileIdTable::GetRecordCount


## -description

Retrieves the number of records that are stored in a similarity file ID table.

## -parameters

### -param recordCount [out]

A pointer to a variable that receives the number of records.

## -returns

Returns <b>S_OK</b> on success, or an error <b>HRESULT</b> on failure.

This method can also return the following error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilarityfileidtable">ISimilarityFileIdTable</a>