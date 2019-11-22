---
UID: NN:msrdc.IFindSimilarResults
title: IFindSimilarResults (msrdc.h)

description: Provides methods for retrieving information from the file list returned by the ISimilarity::FindSimilarFileId method.
old-location: rdc\ifindsimilarresults.htm
tech.root: rdc
ms.assetid: 3118cf53-c544-48bc-ac38-79ca2252f83f

ms.date: 12/05/2018
ms.keywords: IFindSimilarResults, IFindSimilarResults interface [Remote Differential Compression], IFindSimilarResults interface [Remote Differential Compression],described, fs.ifindsimilarresults, msrdc/IFindSimilarResults, rdc.ifindsimilarresults
ms.topic: interface
f1_keywords: 
 - "msrdc/IFindSimilarResults"
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
 - IFindSimilarResults
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFindSimilarResults interface


## -description


Provides methods for retrieving information from the file list returned by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarity-findsimilarfileid">ISimilarity::FindSimilarFileId</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFindSimilarResults</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFindSimilarResults</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFindSimilarResults</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-ifindsimilarresults-getnextfileid">GetNextFileId</a>
</td>
<td align="left" width="63%">
Retrieves the next valid similarity file ID in the file list that was returned by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarity-findsimilarfileid">ISimilarity::FindSimilarFileId</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-ifindsimilarresults-getsize">GetSize</a>
</td>
<td align="left" width="63%">
Retrieves the number of entries in the  file list that was returned by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarity-findsimilarfileid">ISimilarity::FindSimilarFileId</a> method.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarity-findsimilarfileid">ISimilarity::FindSimilarFileId</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

