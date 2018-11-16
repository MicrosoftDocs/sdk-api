---
UID: NN:msrdc.ISimilarityTableDumpState
title: ISimilarityTableDumpState
author: windows-sdk-content
description: Provides a method for retrieving information from the similarity traits list that was returned by the ISimilarityTraitsTable::BeginDump method.
old-location: rdc\isimilaritytabledumpstate.htm
tech.root: Rdc
ms.assetid: a56433b5-191f-49fe-83fb-7057e4c30bbd
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ISimilarityTableDumpState, ISimilarityTableDumpState interface [Remote Differential Compression], ISimilarityTableDumpState interface [Remote Differential Compression],described, fs.isimilaritytabledumpstate, msrdc/ISimilarityTableDumpState, rdc.isimilaritytabledumpstate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - ISimilarityTableDumpState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISimilarityTableDumpState interface


## -description


Provides a method for retrieving information from the similarity traits list that was returned by the <a href="https://msdn.microsoft.com/93298019-334b-4685-b95e-a1081c2bd9dc">ISimilarityTraitsTable::BeginDump</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISimilarityTableDumpState</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISimilarityTableDumpState</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISimilarityTableDumpState</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40ec97fc-052d-474e-9a55-822aa113ac03">GetNextData</a>
</td>
<td align="left" width="63%">
Retrieves one or more <a href="https://msdn.microsoft.com/0200008c-5664-445f-ae65-0eb004856a4c">SimilarityDumpData</a> structures from the similarity traits list.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

