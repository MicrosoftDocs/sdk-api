---
UID: NF:msrdc.ISimilarityFileIdTable.Invalidate
title: ISimilarityFileIdTable::Invalidate
author: windows-sdk-content
description: Marks a file ID as not valid in the similarity file ID table.
old-location: rdc\isimilarityfileidtable_invalidate.htm
old-project: Rdc
ms.assetid: fdd6ff92-d312-4789-b535-4859fa7c871c
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: ISimilarityFileIdTable interface [Remote Differential Compression],Invalidate method, ISimilarityFileIdTable.Invalidate, ISimilarityFileIdTable::Invalidate, Invalidate, Invalidate method [Remote Differential Compression], Invalidate method [Remote Differential Compression],ISimilarityFileIdTable interface, fs.isimilarityfileidtable_invalidate, msrdc/ISimilarityFileIdTable::Invalidate, rdc.isimilarityfileidtable_invalidate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msrdc.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: RdcMappingAccessMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - ISimilarityFileIdTable.Invalidate
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISimilarityFileIdTable::Invalidate


## -description


Marks a file ID as not valid in the similarity file ID table.

This method should be called for files that have been deleted or are otherwise no longer available.


## -parameters




### -param similarityFileIndex [in]

The index of the file ID's entry in the similarity file ID table.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The file ID is marked as not valid by setting the contents of the corresponding  <a href="https://msdn.microsoft.com/07fcb382-726c-4615-83e9-f69eec778311">SimilarityFileId</a> structure to all zeros. A file ID that is marked as not valid will not be included in the results that are returned by the <a href="https://msdn.microsoft.com/70a205fc-d90a-43fc-88f4-2f3a573c5a82">ISimilarity::FindSimilarFileId</a> method.




## -see-also




<a href="https://msdn.microsoft.com/539a2e9b-9719-4012-bb7f-4d14723a3695">ISimilarityFileIdTable</a>
 

 

