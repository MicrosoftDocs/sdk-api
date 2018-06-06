---
UID: NN:tuner.IDVBTuningSpace
title: IDVBTuningSpace
author: windows-sdk-content
description: The IDVBTuningSpace interface is implemented on the DVBTuningSpace object.Note  New applications should use the IDVBTuningSpace2 interface, which inherits IDVBTuningSpace and adds additional methods. .
old-location: mstv\idvbtuningspace.htm
old-project: mstv
ms.assetid: fba3c7f3-61f8-4704-8068-cb1d3171345a
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IDVBTuningSpace, IDVBTuningSpace interface [Microsoft TV Technologies], IDVBTuningSpace interface [Microsoft TV Technologies],described, IDVBTuningSpaceInterface, mstv.idvbtuningspace, tuner/IDVBTuningSpace
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IDVBTuningSpace
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IDVBTuningSpace interface


## -description



The <b>IDVBTuningSpace</b> interface is implemented on the DVBTuningSpace object.

<div class="alert"><b>Note</b>  New applications should use the <a href="https://msdn.microsoft.com/01325520-0cb3-46c2-b5a1-f07c5f8d7c7b">IDVBTuningSpace2</a> interface, which inherits <b>IDVBTuningSpace</b> and adds additional methods.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDVBTuningSpace</b> interface inherits from <a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace</a>. <b>IDVBTuningSpace</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDVBTuningSpace</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e08d142-6ae3-4da7-ba3c-59fdf07a2f10">get_SystemType</a>
</td>
<td align="left" width="63%">
Retrieves the DVB system type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/559f882a-4d1c-4fe1-af21-b3ad7ccd3ff2">put_SystemType</a>
</td>
<td align="left" width="63%">
Sets the DVB system type.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IDVBTuningSpace)</code>.




## -see-also




<a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

