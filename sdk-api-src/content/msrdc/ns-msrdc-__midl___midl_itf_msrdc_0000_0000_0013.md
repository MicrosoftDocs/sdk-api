---
UID: NS:msrdc.__MIDL___MIDL_itf_msrdc_0000_0000_0013
title: "__MIDL___MIDL_itf_msrdc_0000_0000_0013"
author: windows-sdk-content
description: Contains the file index information that the ISimilarityTraitsTable::FindSimilarFileIndex method returned for a matching file.
old-location: rdc\findsimilarfileindexresults.htm
old-project: Rdc
ms.assetid: 2e0d39ab-d491-496e-8753-e7223a5c5029
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: FindSimilarFileIndexResults, FindSimilarFileIndexResults structure [Remote Differential Compression], __MIDL___MIDL_itf_msrdc_0000_0000_0013, fs.findsimilarfileindexresults, msrdc/FindSimilarFileIndexResults, rdc.findsimilarfileindexresults
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: FindSimilarFileIndexResults
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - MsRdc.h
api_name:
 - FindSimilarFileIndexResults
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# __MIDL___MIDL_itf_msrdc_0000_0000_0013 structure


## -description


Contains the file index information that the <a href="https://msdn.microsoft.com/09c9b918-1def-4d19-84d4-99b881070e36">ISimilarityTraitsTable::FindSimilarFileIndex</a> method returned for a matching file.


## -struct-fields




### -field m_FileIndex

The index of the matching file in the similarity traits table.


### -field m_MatchCount

The number of traits that were matched. The valid range is from <b>MSRDC_MINIMUM_MATCHESREQUIRED</b> to 
      <b>MSRDC_MAXIMUM_MATCHESREQUIRED</b>.


## -see-also




<a href="https://msdn.microsoft.com/09c9b918-1def-4d19-84d4-99b881070e36">ISimilarityTraitsTable::FindSimilarFileIndex</a>
 

 

