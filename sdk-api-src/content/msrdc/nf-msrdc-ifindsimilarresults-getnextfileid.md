---
UID: NF:msrdc.IFindSimilarResults.GetNextFileId
title: IFindSimilarResults::GetNextFileId
author: windows-driver-content
description: Retrieves the next valid similarity file ID in the file list that was returned by the ISimilarity::FindSimilarFileId method.
old-location: rdc\ifindsimilarresults_getnextfileid.htm
old-project: Rdc
ms.assetid: 881e0ae6-311f-4bc4-9660-b0e96b7b9bd2
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetNextFileId, GetNextFileId method [Remote Differential Compression], GetNextFileId method [Remote Differential Compression],IFindSimilarResults interface, IFindSimilarResults interface [Remote Differential Compression],GetNextFileId method, IFindSimilarResults.GetNextFileId, IFindSimilarResults::GetNextFileId, fs.ifindsimilarresults_getnextfileid, msrdc/IFindSimilarResults::GetNextFileId, rdc.ifindsimilarresults_getnextfileid
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: RdcMappingAccessMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	MsRdc.dll
api_name:
-	IFindSimilarResults.GetNextFileId
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IFindSimilarResults::GetNextFileId


## -description


Retrieves the next valid similarity file ID in the file list that was returned by the <a href="https://msdn.microsoft.com/70a205fc-d90a-43fc-88f4-2f3a573c5a82">ISimilarity::FindSimilarFileId</a> method.


## -parameters




### -param numTraitsMatched [out]

A pointer to a variable that receives the number of traits that were matched.


### -param similarityFileId [out]

A pointer to a <a href="https://msdn.microsoft.com/07fcb382-726c-4615-83e9-f69eec778311">SimilarityFileId</a> structure that contains the similarity file ID of the matching file.


## -returns



Returns <b>S_OK</b> on success, or an error <b>HRESULT</b> on failure.

This method can also return the following error code.




## -see-also




<a href="https://msdn.microsoft.com/3118cf53-c544-48bc-ac38-79ca2252f83f">IFindSimilarResults</a>
 

 

