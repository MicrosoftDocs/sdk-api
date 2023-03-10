---
UID: NF:msrdc.ISimilarityFileIdTable.Invalidate
title: ISimilarityFileIdTable::Invalidate (msrdc.h)
description: Marks a file ID as not valid in the similarity file ID table.
helpviewer_keywords: ["ISimilarityFileIdTable interface [Remote Differential Compression]","Invalidate method","ISimilarityFileIdTable.Invalidate","ISimilarityFileIdTable::Invalidate","Invalidate","Invalidate method [Remote Differential Compression]","Invalidate method [Remote Differential Compression]","ISimilarityFileIdTable interface","fs.isimilarityfileidtable_invalidate","msrdc/ISimilarityFileIdTable::Invalidate","rdc.isimilarityfileidtable_invalidate"]
old-location: rdc\isimilarityfileidtable_invalidate.htm
tech.root: rdc
ms.assetid: fdd6ff92-d312-4789-b535-4859fa7c871c
ms.date: 12/05/2018
ms.keywords: ISimilarityFileIdTable interface [Remote Differential Compression],Invalidate method, ISimilarityFileIdTable.Invalidate, ISimilarityFileIdTable::Invalidate, Invalidate, Invalidate method [Remote Differential Compression], Invalidate method [Remote Differential Compression],ISimilarityFileIdTable interface, fs.isimilarityfileidtable_invalidate, msrdc/ISimilarityFileIdTable::Invalidate, rdc.isimilarityfileidtable_invalidate
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
 - ISimilarityFileIdTable::Invalidate
 - msrdc/ISimilarityFileIdTable::Invalidate
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
 - ISimilarityFileIdTable.Invalidate
---

# ISimilarityFileIdTable::Invalidate


## -description

Marks a file ID as not valid in the similarity file ID table.

This method should be called for files that have been deleted or are otherwise no longer available.

## -parameters

### -param similarityFileIndex [in]

The index of the file ID's entry in the similarity file ID table.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The file ID is marked as not valid by setting the contents of the corresponding  <a href="/windows/win32/api/msrdc/ns-msrdc-similarityfileid">SimilarityFileId</a> structure to all zeros. A file ID that is marked as not valid will not be included in the results that are returned by the <a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarity-findsimilarfileid">ISimilarity::FindSimilarFileId</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilarityfileidtable">ISimilarityFileIdTable</a>