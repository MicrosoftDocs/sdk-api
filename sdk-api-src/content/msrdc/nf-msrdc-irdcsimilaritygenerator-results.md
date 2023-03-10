---
UID: NF:msrdc.IRdcSimilarityGenerator.Results
title: IRdcSimilarityGenerator::Results (msrdc.h)
description: Retrieves the similarity data that was generated for a file by the signature generator.
helpviewer_keywords: ["IRdcSimilarityGenerator interface [Remote Differential Compression]","Results method","IRdcSimilarityGenerator.Results","IRdcSimilarityGenerator::Results","Results","Results method [Remote Differential Compression]","Results method [Remote Differential Compression]","IRdcSimilarityGenerator interface","fs.irdcsimilaritygenerator_results","msrdc/IRdcSimilarityGenerator::Results","rdc.irdcsimilaritygenerator_results"]
old-location: rdc\irdcsimilaritygenerator_results.htm
tech.root: rdc
ms.assetid: 572c38e2-0bd4-427e-9ba3-f69539410d4d
ms.date: 12/05/2018
ms.keywords: IRdcSimilarityGenerator interface [Remote Differential Compression],Results method, IRdcSimilarityGenerator.Results, IRdcSimilarityGenerator::Results, Results, Results method [Remote Differential Compression], Results method [Remote Differential Compression],IRdcSimilarityGenerator interface, fs.irdcsimilaritygenerator_results, msrdc/IRdcSimilarityGenerator::Results, rdc.irdcsimilaritygenerator_results
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRdcSimilarityGenerator::Results
 - msrdc/IRdcSimilarityGenerator::Results
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - IRdcSimilarityGenerator.Results
---

# IRdcSimilarityGenerator::Results


## -description

Retrieves the similarity data that was generated for a file by the signature generator.

This method cannot be called until signature generation is completed. For more information, see the <i>endOfOutput</i> parameter of the <a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcgenerator-process">IRdcGenerator::Process</a> method.

## -parameters

### -param similarityData [out]

A pointer to a <a href="/windows/win32/api/msrdc/ns-msrdc-similaritydata">SimilarityData</a> structure that will receive the similarity data.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcsimilaritygenerator">IRdcSimilarityGenerator</a>