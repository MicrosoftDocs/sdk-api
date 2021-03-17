---
UID: NF:msrdc.ISimilarity.Append
title: ISimilarity::Append (msrdc.h)
description: Adds the file ID and similarity data information to the tables in the similarity file.
helpviewer_keywords: ["Append","Append method [Remote Differential Compression]","Append method [Remote Differential Compression]","ISimilarity interface","ISimilarity interface [Remote Differential Compression]","Append method","ISimilarity.Append","ISimilarity::Append","fs.isimilarity_append","msrdc/ISimilarity::Append","rdc.isimilarity_append"]
old-location: rdc\isimilarity_append.htm
tech.root: rdc
ms.assetid: f8896d9e-ca6a-404f-b80f-ef739ec97b53
ms.date: 12/05/2018
ms.keywords: Append, Append method [Remote Differential Compression], Append method [Remote Differential Compression],ISimilarity interface, ISimilarity interface [Remote Differential Compression],Append method, ISimilarity.Append, ISimilarity::Append, fs.isimilarity_append, msrdc/ISimilarity::Append, rdc.isimilarity_append
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
 - ISimilarity::Append
 - msrdc/ISimilarity::Append
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
 - ISimilarity.Append
---

# ISimilarity::Append


## -description

Adds the file ID and similarity data information to the tables in the similarity file.

## -parameters

### -param similarityFileId [in]

A pointer to the <a href="/windows/win32/api/msrdc/ns-msrdc-similarityfileid">SimilarityFileId</a> structure to be added to the similarity file ID table.

### -param similarityData [in]

A pointer to the <a href="/windows/win32/api/msrdc/ns-msrdc-similaritydata">SimilarityData</a> structure to be added to the similarity traits table.

## -returns

Returns <b>S_OK</b> on success, or an error <b>HRESULT</b> on failure.

This method can also return the following error codes.

## -remarks

If this method fails, the similarity file ID table and the similarity traits table are marked as corrupted and must be rebuilt by the application. The application must close the corrupted tables and create new tables.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilarity">ISimilarity</a>