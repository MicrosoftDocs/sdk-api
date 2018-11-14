---
UID: NN:tuner.IDVBTuningSpace2
title: IDVBTuningSpace2
author: windows-sdk-content
description: The IDVBTuningSpace2 interface is implemented on the DVBTuningSpace object. It provides methods for working with tuning spaces with a network type of DVB.
old-location: mstv\idvbtuningspace2.htm
tech.root: MSTV
ms.assetid: 01325520-0cb3-46c2-b5a1-f07c5f8d7c7b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDVBTuningSpace2, IDVBTuningSpace2 interface [Microsoft TV Technologies], IDVBTuningSpace2 interface [Microsoft TV Technologies],described, IDVBTuningSpace2Interface, mstv.idvbtuningspace2, tuner/IDVBTuningSpace2
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IDVBTuningSpace2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDVBTuningSpace2 interface


## -description



The <b>IDVBTuningSpace2</b> interface is implemented on the DVBTuningSpace object. It provides methods for working with tuning spaces with a network type of DVB.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDVBTuningSpace2</b> interface inherits from <a href="https://msdn.microsoft.com/fba3c7f3-61f8-4704-8068-cb1d3171345a">IDVBTuningSpace</a>. <b>IDVBTuningSpace2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDVBTuningSpace2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/743977d3-151d-4d04-8d2d-7018d5613cc1">get_NetworkID</a>
</td>
<td align="left" width="63%">
Gets the network ID of the DVB system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f307629-710d-4992-b407-311774aa544a">put_NetworkID</a>
</td>
<td align="left" width="63%">
Sets the network ID of the DVB system

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IDVBTuningSpace2)</code>.




## -see-also




<a href="https://msdn.microsoft.com/fba3c7f3-61f8-4704-8068-cb1d3171345a">IDVBTuningSpace</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

