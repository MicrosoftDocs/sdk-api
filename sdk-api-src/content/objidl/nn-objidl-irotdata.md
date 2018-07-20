---
UID: NN:objidl.IROTData
title: IROTData
author: windows-sdk-content
description: Implemented by monikers to enable the running object table (ROT) to compare monikers against each other.
old-location: com\irotdata.htm
old-project: com
ms.assetid: 44ae8377-c375-4dc3-9f54-a5674e24763f
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IROTData, IROTData interface [COM], IROTData interface [COM],described, _com_irotdata, com.irotdata, objidl/IROTData
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IROTData
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# IROTData interface


## -description


Implemented by monikers to enable the running object table (ROT) to compare monikers against each other.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IROTData</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IROTData</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IROTData</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7f2d3a6-2517-47bc-aa6a-509d72881a0b">GetComparisonData</a>
</td>
<td align="left" width="63%">
Retrieves data from a moniker that can be used to test the moniker for equality against another moniker.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a>



<a href="https://msdn.microsoft.com/ff89bcb5-df6d-4325-b0e8-613217a68f42">IRunningObjectTable</a>
 

 

