---
UID: NF:msrdc.IRdcSimilarityGenerator.EnableSimilarity
title: IRdcSimilarityGenerator::EnableSimilarity (msrdc.h)
description: Enables the signature generator to generate similarity data.
helpviewer_keywords: ["EnableSimilarity","EnableSimilarity method [Remote Differential Compression]","EnableSimilarity method [Remote Differential Compression]","IRdcSimilarityGenerator interface","IRdcSimilarityGenerator interface [Remote Differential Compression]","EnableSimilarity method","IRdcSimilarityGenerator.EnableSimilarity","IRdcSimilarityGenerator::EnableSimilarity","fs.irdcsimilaritygenerator_enablesimilarity","msrdc/IRdcSimilarityGenerator::EnableSimilarity","rdc.irdcsimilaritygenerator_enablesimilarity"]
old-location: rdc\irdcsimilaritygenerator_enablesimilarity.htm
tech.root: rdc
ms.assetid: 1d67be55-ed00-4e41-9319-10947d1d88a0
ms.date: 12/05/2018
ms.keywords: EnableSimilarity, EnableSimilarity method [Remote Differential Compression], EnableSimilarity method [Remote Differential Compression],IRdcSimilarityGenerator interface, IRdcSimilarityGenerator interface [Remote Differential Compression],EnableSimilarity method, IRdcSimilarityGenerator.EnableSimilarity, IRdcSimilarityGenerator::EnableSimilarity, fs.irdcsimilaritygenerator_enablesimilarity, msrdc/IRdcSimilarityGenerator::EnableSimilarity, rdc.irdcsimilaritygenerator_enablesimilarity
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
 - IRdcSimilarityGenerator::EnableSimilarity
 - msrdc/IRdcSimilarityGenerator::EnableSimilarity
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
 - IRdcSimilarityGenerator.EnableSimilarity
---

# IRdcSimilarityGenerator::EnableSimilarity


## -description

Enables the signature generator to generate similarity data.

The <b>EnableSimilarity</b> method must be called before the <a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcgenerator-process">IRdcGenerator::Process</a> method is called to begin generating signatures. Otherwise, this method will return an error.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcsimilaritygenerator">IRdcSimilarityGenerator</a>
