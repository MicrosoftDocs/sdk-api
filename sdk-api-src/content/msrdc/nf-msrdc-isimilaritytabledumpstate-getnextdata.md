---
UID: NF:msrdc.ISimilarityTableDumpState.GetNextData
title: ISimilarityTableDumpState::GetNextData (msrdc.h)
author: windows-sdk-content
description: Retrieves one or more SimilarityDumpData structures from the similarity traits list that was returned by the ISimilarityTraitsTable::BeginDump method.
old-location: rdc\isimilaritytabledumpstate_getnextdata.htm
tech.root: rdc
ms.assetid: 40ec97fc-052d-474e-9a55-822aa113ac03
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetNextData, GetNextData method [Remote Differential Compression], GetNextData method [Remote Differential Compression],ISimilarityTableDumpState interface, ISimilarityTableDumpState interface [Remote Differential Compression],GetNextData method, ISimilarityTableDumpState.GetNextData, ISimilarityTableDumpState::GetNextData, fs.isimilaritytabledumpstate_getnextdata, msrdc/ISimilarityTableDumpState::GetNextData, rdc.isimilaritytabledumpstate_getnextdata
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
 - ISimilarityTableDumpState.GetNextData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISimilarityTableDumpState::GetNextData


## -description


Retrieves one or more <a href="https://msdn.microsoft.com/0200008c-5664-445f-ae65-0eb004856a4c">SimilarityDumpData</a> structures from the similarity traits list that was returned by the <a href="https://msdn.microsoft.com/93298019-334b-4685-b95e-a1081c2bd9dc">ISimilarityTraitsTable::BeginDump</a> method.


## -parameters




### -param resultsSize [in]

The number of <a href="https://msdn.microsoft.com/0200008c-5664-445f-ae65-0eb004856a4c">SimilarityDumpData</a> structures that can be stored in the buffer that the <i>results</i> parameter points to.


### -param resultsUsed [out]

A pointer to a variable that receives the number of <a href="https://msdn.microsoft.com/0200008c-5664-445f-ae65-0eb004856a4c">SimilarityDumpData</a> structures that were returned in the buffer that the <i>results</i> parameter points to.


### -param eof [out]

A pointer to a variable that receives <b>TRUE</b> if the end of the file is reached; otherwise, <b>FALSE</b>.


### -param results [in, out]

A pointer to a buffer that receives the <a href="https://msdn.microsoft.com/0200008c-5664-445f-ae65-0eb004856a4c">SimilarityDumpData</a> structures.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a56433b5-191f-49fe-83fb-7057e4c30bbd">ISimilarityTableDumpState</a>
 

 

