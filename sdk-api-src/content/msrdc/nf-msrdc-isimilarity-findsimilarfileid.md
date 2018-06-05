---
UID: NF:msrdc.ISimilarity.FindSimilarFileId
title: ISimilarity::FindSimilarFileId
author: windows-sdk-content
description: Returns a list of files that are similar to a given file.
old-location: rdc\isimilarity_findsimilarfileid.htm
old-project: Rdc
ms.assetid: 70a205fc-d90a-43fc-88f4-2f3a573c5a82
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: FindSimilarFileId, FindSimilarFileId method [Remote Differential Compression], FindSimilarFileId method [Remote Differential Compression],ISimilarity interface, ISimilarity interface [Remote Differential Compression],FindSimilarFileId method, ISimilarity.FindSimilarFileId, ISimilarity::FindSimilarFileId, fs.isimilarity_findsimilarfileid, msrdc/ISimilarity::FindSimilarFileId, rdc.isimilarity_findsimilarfileid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: RdcMappingAccessMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	MsRdc.dll
api_name:
-	ISimilarity.FindSimilarFileId
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISimilarity::FindSimilarFileId


## -description


Returns a list of files that are similar to a given file.


## -parameters




### -param similarityData [in]

A pointer to a <a href="https://msdn.microsoft.com/33fdb48c-6f33-44e8-83b1-6029b1eace1d">SimilarityData</a> structure that contains similarity information for the file.


### -param numberOfMatchesRequired




### -param resultsSize [in]

The number of file IDs that can be stored in the <a href="https://msdn.microsoft.com/3118cf53-c544-48bc-ac38-79ca2252f83f">IFindSimilarResults</a> object that the <i>findSimilarResults</i> parameter points to.


### -param findSimilarResults [out, optional]

A pointer to a location that will receive the returned  <a href="https://msdn.microsoft.com/3118cf53-c544-48bc-ac38-79ca2252f83f">IFindSimilarResults</a> interface pointer. The caller must release this interface when it is no longer needed.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The file IDs that are returned in the <i>findSimilarResults</i> parameter may include IDs of files that have been deleted.




## -see-also




<a href="https://msdn.microsoft.com/fe0cd874-a40c-4d82-99bf-b84008a4995c">ISimilarity</a>
 

 

