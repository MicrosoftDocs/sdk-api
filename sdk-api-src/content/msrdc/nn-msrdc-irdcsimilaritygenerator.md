---
UID: NN:msrdc.IRdcSimilarityGenerator
title: IRdcSimilarityGenerator (msrdc.h)
description: Defines methods for enabling the signature generator to generate similarity data and for retrieving the similarity data after it is generated.
helpviewer_keywords: ["IRdcSimilarityGenerator","IRdcSimilarityGenerator interface [Remote Differential Compression]","IRdcSimilarityGenerator interface [Remote Differential Compression]","described","fs.irdcsimilaritygenerator","msrdc/IRdcSimilarityGenerator","rdc.irdcsimilaritygenerator"]
old-location: rdc\irdcsimilaritygenerator.htm
tech.root: rdc
ms.assetid: 60133763-9678-4927-9d3a-3e431310b601
ms.date: 12/05/2018
ms.keywords: IRdcSimilarityGenerator, IRdcSimilarityGenerator interface [Remote Differential Compression], IRdcSimilarityGenerator interface [Remote Differential Compression],described, fs.irdcsimilaritygenerator, msrdc/IRdcSimilarityGenerator, rdc.irdcsimilaritygenerator
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
 - IRdcSimilarityGenerator
 - msrdc/IRdcSimilarityGenerator
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
 - IRdcSimilarityGenerator
---

# IRdcSimilarityGenerator interface


## -description

Defines methods for enabling the signature generator to generate similarity data and for retrieving the similarity data after it is generated.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRdcSimilarityGenerator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRdcSimilarityGenerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRdcSimilarityGenerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcsimilaritygenerator-enablesimilarity">EnableSimilarity</a>
</td>
<td align="left" width="63%">
Enables the signature generator to generate similarity data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcsimilaritygenerator-results">Results</a>
</td>
<td align="left" width="63%">
Retrieves the similarity data that was generated for a file by the signature generator.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>