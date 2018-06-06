---
UID: NF:msrdc.ISimilarity.Append
title: ISimilarity::Append
author: windows-sdk-content
description: Adds the file ID and similarity data information to the tables in the similarity file.
old-location: rdc\isimilarity_append.htm
old-project: Rdc
ms.assetid: f8896d9e-ca6a-404f-b80f-ef739ec97b53
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: Append, Append method [Remote Differential Compression], Append method [Remote Differential Compression],ISimilarity interface, ISimilarity interface [Remote Differential Compression],Append method, ISimilarity.Append, ISimilarity::Append, fs.isimilarity_append, msrdc/ISimilarity::Append, rdc.isimilarity_append
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - ISimilarity.Append
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISimilarity::Append


## -description


Adds the file ID and similarity data information to the tables in the similarity file.


## -parameters




### -param similarityFileId [in]

A pointer to the <a href="https://msdn.microsoft.com/07fcb382-726c-4615-83e9-f69eec778311">SimilarityFileId</a> structure to be added to the similarity file ID table.


### -param similarityData [in]

A pointer to the <a href="https://msdn.microsoft.com/33fdb48c-6f33-44e8-83b1-6029b1eace1d">SimilarityData</a> structure to be added to the similarity traits table.


## -returns



Returns <b>S_OK</b> on success, or an error <b>HRESULT</b> on failure.

This method can also return the following error codes.




## -remarks



If this method fails, the similarity file ID table and the similarity traits table are marked as corrupted and must be rebuilt by the application. The application must close the corrupted tables and create new tables.




## -see-also




<a href="https://msdn.microsoft.com/fe0cd874-a40c-4d82-99bf-b84008a4995c">ISimilarity</a>
 

 

