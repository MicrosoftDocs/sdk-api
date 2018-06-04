---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

