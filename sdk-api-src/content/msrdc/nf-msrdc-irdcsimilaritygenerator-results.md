---
UID: NF:msrdc.IRdcSimilarityGenerator.Results
title: IRdcSimilarityGenerator::Results (msrdc.h)
author: windows-sdk-content
description: Retrieves the similarity data that was generated for a file by the signature generator.
old-location: rdc\irdcsimilaritygenerator_results.htm
tech.root: rdc
ms.assetid: 572c38e2-0bd4-427e-9ba3-f69539410d4d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRdcSimilarityGenerator interface [Remote Differential Compression],Results method, IRdcSimilarityGenerator.Results, IRdcSimilarityGenerator::Results, Results, Results method [Remote Differential Compression], Results method [Remote Differential Compression],IRdcSimilarityGenerator interface, fs.irdcsimilaritygenerator_results, msrdc/IRdcSimilarityGenerator::Results, rdc.irdcsimilaritygenerator_results
ms.topic: method
f1_keywords: 
 - "msrdc/IRdcSimilarityGenerator.Results"
dev_langs:
 - c++
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
 - IRdcSimilarityGenerator.Results
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRdcSimilarityGenerator::Results


## -description


Retrieves the similarity data that was generated for a file by the signature generator.

This method cannot be called until signature generation is completed. For more information, see the <i>endOfOutput</i> parameter of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcgenerator-process">IRdcGenerator::Process</a> method.


## -parameters




### -param similarityData [out]

A pointer to a <a href="https://docs.microsoft.com/windows/win32/api/msrdc/ns-msrdc-similaritydata">SimilarityData</a> structure that will receive the similarity data.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcsimilaritygenerator">IRdcSimilarityGenerator</a>
 

 

