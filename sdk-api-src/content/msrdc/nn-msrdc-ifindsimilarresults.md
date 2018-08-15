---
UID: NN:msrdc.IFindSimilarResults
title: IFindSimilarResults
author: windows-sdk-content
description: Provides methods for retrieving information from the file list returned by the ISimilarity::FindSimilarFileId method.
old-location: rdc\ifindsimilarresults.htm
old-project: Rdc
ms.assetid: 3118cf53-c544-48bc-ac38-79ca2252f83f
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IFindSimilarResults, IFindSimilarResults interface [Remote Differential Compression], IFindSimilarResults interface [Remote Differential Compression],described, fs.ifindsimilarresults, msrdc/IFindSimilarResults, rdc.ifindsimilarresults
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msrdc.h
req.include-header: 
req.redist: 
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
req.typenames: RdcMappingAccessMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - IFindSimilarResults
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IFindSimilarResults interface


## -description


Provides methods for retrieving information from the file list returned by the <a href="https://msdn.microsoft.com/70a205fc-d90a-43fc-88f4-2f3a573c5a82">ISimilarity::FindSimilarFileId</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFindSimilarResults</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFindSimilarResults</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/881e0ae6-311f-4bc4-9660-b0e96b7b9bd2">GetNextFileId</a>
</td>
<td align="left" width="63%">
Retrieves the next valid similarity file ID in the file list that was returned by the <a href="https://msdn.microsoft.com/70a205fc-d90a-43fc-88f4-2f3a573c5a82">ISimilarity::FindSimilarFileId</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c59a6fb0-e81f-4b7d-b0e6-9a5c9730fa9d">GetSize</a>
</td>
<td align="left" width="63%">
Retrieves the number of entries in the  file list that was returned by the <a href="https://msdn.microsoft.com/70a205fc-d90a-43fc-88f4-2f3a573c5a82">ISimilarity::FindSimilarFileId</a> method.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/70a205fc-d90a-43fc-88f4-2f3a573c5a82">ISimilarity::FindSimilarFileId</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

