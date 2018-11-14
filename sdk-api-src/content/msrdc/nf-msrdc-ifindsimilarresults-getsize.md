---
UID: NF:msrdc.IFindSimilarResults.GetSize
title: IFindSimilarResults::GetSize
author: windows-sdk-content
description: Retrieves the number of entries in the file list that was returned by the ISimilarity::FindSimilarFileId method.
old-location: rdc\ifindsimilarresults_getsize.htm
tech.root: Rdc
ms.assetid: c59a6fb0-e81f-4b7d-b0e6-9a5c9730fa9d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetSize, GetSize method [Remote Differential Compression], GetSize method [Remote Differential Compression],IFindSimilarResults interface, IFindSimilarResults interface [Remote Differential Compression],GetSize method, IFindSimilarResults.GetSize, IFindSimilarResults::GetSize, fs.ifindsimilarresults_getsize, msrdc/IFindSimilarResults::GetSize, rdc.ifindsimilarresults_getsize
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
req.lib: 
req.dll: MsRdc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - IFindSimilarResults.GetSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- msrdc.h
: 
- IFindSimilarResults.GetSize
: 
---

# IFindSimilarResults::GetSize


## -description


Retrieves the number of entries in the  file list that was returned by the <a href="https://msdn.microsoft.com/70a205fc-d90a-43fc-88f4-2f3a573c5a82">ISimilarity::FindSimilarFileId</a> method.

The actual number of similarity file IDs that are returned by the <a href="https://msdn.microsoft.com/881e0ae6-311f-4bc4-9660-b0e96b7b9bd2">GetNextFileId</a> method may be less than the number that is  returned by the <b>GetSize</b>  method.  <b>GetNextFileId</b> returns only valid similarity file IDs. However, <b>GetSize</b> counts all entries, even if their similarity file IDs are not valid.


## -parameters




### -param size [out]

A pointer to a variable that receives the number of entries in the file list.


## -returns



This method always returns <b>S_OK</b>.




## -see-also




<a href="https://msdn.microsoft.com/3118cf53-c544-48bc-ac38-79ca2252f83f">IFindSimilarResults</a>
 

 

