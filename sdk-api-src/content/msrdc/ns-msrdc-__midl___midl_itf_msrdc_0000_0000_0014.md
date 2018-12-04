---
UID: NS:msrdc.__MIDL___MIDL_itf_msrdc_0000_0000_0014
title: "__MIDL___MIDL_itf_msrdc_0000_0000_0014"
author: windows-sdk-content
description: Contains the similarity information that was returned for a file by the ISimilarityTableDumpState::GetNextData method.
old-location: rdc\similaritydumpdata.htm
tech.root: rdc
ms.assetid: 0200008c-5664-445f-ae65-0eb004856a4c
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: SimilarityDumpData, SimilarityDumpData structure [Remote Differential Compression], __MIDL___MIDL_itf_msrdc_0000_0000_0014, fs.similaritydumpdata, msrdc/SimilarityDumpData, rdc.similaritydumpdata
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - MsRdc.h
api_name:
 - SimilarityDumpData
product: Windows
targetos: Windows
req.typenames: SimilarityDumpData
req.redist: 
---

# __MIDL___MIDL_itf_msrdc_0000_0000_0014 structure


## -description


Contains the similarity information that was returned for a file by the <a href="https://msdn.microsoft.com/40ec97fc-052d-474e-9a55-822aa113ac03">ISimilarityTableDumpState::GetNextData</a> method.


## -struct-fields




### -field m_FileIndex

The index of the <a href="https://msdn.microsoft.com/33fdb48c-6f33-44e8-83b1-6029b1eace1d">SimilarityData</a> structure in the similarity traits table.


### -field m_Data

A <a href="https://msdn.microsoft.com/33fdb48c-6f33-44e8-83b1-6029b1eace1d">SimilarityData</a> structure that contains the similarity data for the file.


## -see-also




<a href="https://msdn.microsoft.com/a56433b5-191f-49fe-83fb-7057e4c30bbd">ISimilarityTableDumpState</a>
 

 

