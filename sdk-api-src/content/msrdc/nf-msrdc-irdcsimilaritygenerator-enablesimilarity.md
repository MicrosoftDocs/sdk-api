---
UID: NF:msrdc.IRdcSimilarityGenerator.EnableSimilarity
title: IRdcSimilarityGenerator::EnableSimilarity
author: windows-sdk-content
description: Enables the signature generator to generate similarity data.
old-location: rdc\irdcsimilaritygenerator_enablesimilarity.htm
old-project: Rdc
ms.assetid: 1d67be55-ed00-4e41-9319-10947d1d88a0
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: EnableSimilarity, EnableSimilarity method [Remote Differential Compression], EnableSimilarity method [Remote Differential Compression],IRdcSimilarityGenerator interface, IRdcSimilarityGenerator interface [Remote Differential Compression],EnableSimilarity method, IRdcSimilarityGenerator.EnableSimilarity, IRdcSimilarityGenerator::EnableSimilarity, fs.irdcsimilaritygenerator_enablesimilarity, msrdc/IRdcSimilarityGenerator::EnableSimilarity, rdc.irdcsimilaritygenerator_enablesimilarity
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
req.typenames: RdcMappingAccessMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	MsRdc.dll
api_name:
-	IRdcSimilarityGenerator.EnableSimilarity
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IRdcSimilarityGenerator::EnableSimilarity


## -description


Enables the signature generator to generate similarity data.

The <b>EnableSimilarity</b> method must be called before the <a href="https://msdn.microsoft.com/34d19eee-0fa9-4ac3-a33b-9f01cfa06371">IRdcGenerator::Process</a> method is called to begin generating signatures. Otherwise, this method will return an error.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/60133763-9678-4927-9d3a-3e431310b601">IRdcSimilarityGenerator</a>
 

 

