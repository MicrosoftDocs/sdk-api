---
UID: NF:msrdc.ISimilarityFileIdTable.Lookup
title: ISimilarityFileIdTable::Lookup (msrdc.h)
description: Retrieves the file ID that corresponds to a given file index in the similarity file ID table.
helpviewer_keywords: ["ISimilarityFileIdTable interface [Remote Differential Compression]","Lookup method","ISimilarityFileIdTable.Lookup","ISimilarityFileIdTable::Lookup","Lookup","Lookup method [Remote Differential Compression]","Lookup method [Remote Differential Compression]","ISimilarityFileIdTable interface","fs.isimilarityfileidtable_lookup","msrdc/ISimilarityFileIdTable::Lookup","rdc.isimilarityfileidtable_lookup"]
old-location: rdc\isimilarityfileidtable_lookup.htm
tech.root: rdc
ms.assetid: bf9dbeb1-0182-4927-80ad-bb51fab2e637
ms.date: 12/05/2018
ms.keywords: ISimilarityFileIdTable interface [Remote Differential Compression],Lookup method, ISimilarityFileIdTable.Lookup, ISimilarityFileIdTable::Lookup, Lookup, Lookup method [Remote Differential Compression], Lookup method [Remote Differential Compression],ISimilarityFileIdTable interface, fs.isimilarityfileidtable_lookup, msrdc/ISimilarityFileIdTable::Lookup, rdc.isimilarityfileidtable_lookup
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
 - ISimilarityFileIdTable::Lookup
 - msrdc/ISimilarityFileIdTable::Lookup
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
 - ISimilarityFileIdTable.Lookup
---

# ISimilarityFileIdTable::Lookup


## -description

Retrieves the file ID that corresponds to a given file index in the similarity file ID table.

## -parameters

### -param similarityFileIndex [in]

The file index that was previously returned for the file ID by the <a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarityfileidtable-append">ISimilarityFileIdTable::Append</a> method.

### -param similarityFileId [out]

A pointer to a variable that receives the file ID. If the file has been marked as not valid, the file ID receives zero.

## -returns

Returns <b>S_OK</b> on success, or an error <b>HRESULT</b> on failure.

This method can also return the following error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilarityfileidtable">ISimilarityFileIdTable</a>