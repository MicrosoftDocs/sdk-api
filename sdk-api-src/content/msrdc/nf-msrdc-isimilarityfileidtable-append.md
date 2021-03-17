---
UID: NF:msrdc.ISimilarityFileIdTable.Append
title: ISimilarityFileIdTable::Append (msrdc.h)
description: Adds the file ID to the similarity file ID table.
helpviewer_keywords: ["Append","Append method [Remote Differential Compression]","Append method [Remote Differential Compression]","ISimilarityFileIdTable interface","ISimilarityFileIdTable interface [Remote Differential Compression]","Append method","ISimilarityFileIdTable.Append","ISimilarityFileIdTable::Append","fs.isimilarityfileidtable_append","msrdc/ISimilarityFileIdTable::Append","rdc.isimilarityfileidtable_append"]
old-location: rdc\isimilarityfileidtable_append.htm
tech.root: rdc
ms.assetid: 2157d6e6-0d60-45a2-9f5c-4096088cb2bb
ms.date: 12/05/2018
ms.keywords: Append, Append method [Remote Differential Compression], Append method [Remote Differential Compression],ISimilarityFileIdTable interface, ISimilarityFileIdTable interface [Remote Differential Compression],Append method, ISimilarityFileIdTable.Append, ISimilarityFileIdTable::Append, fs.isimilarityfileidtable_append, msrdc/ISimilarityFileIdTable::Append, rdc.isimilarityfileidtable_append
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
 - ISimilarityFileIdTable::Append
 - msrdc/ISimilarityFileIdTable::Append
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
 - ISimilarityFileIdTable.Append
---

# ISimilarityFileIdTable::Append


## -description

Adds the file ID to the similarity file ID table.

## -parameters

### -param similarityFileId [in]

The file ID to be added to the similarity file ID table.

### -param similarityFileIndex [out]

A pointer to a variable that receives the file index for the file ID's entry in the similarity file ID table.

## -returns

Returns <b>S_OK</b> on success, or an error <b>HRESULT</b> on failure.

This method can also return the following error codes.

## -remarks

If the <b>Append</b> method fails, the similarity file ID table is marked as corrupted and must be rebuilt.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilarityfileidtable">ISimilarityFileIdTable</a>