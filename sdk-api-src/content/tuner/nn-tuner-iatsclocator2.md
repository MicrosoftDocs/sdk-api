---
UID: NN:tuner.IATSCLocator2
title: IATSCLocator2
author: windows-sdk-content
description: The IATASCLocator2 interface enables the network provider to determine the physical channel, transport stream ID, and program number of an ATSC transmission.
old-location: mstv\iatsclocator2.htm
old-project: mstv
ms.assetid: dbb830bf-db46-4981-8a96-ae33b1de3883
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IATSCLocator2, IATSCLocator2 interface [Microsoft TV Technologies], IATSCLocator2 interface [Microsoft TV Technologies],described, IATSCLocator2Interface, mstv.iatsclocator2, tuner/IATSCLocator2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - IATSCLocator2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IATSCLocator2 interface


## -description



The <b>IATASCLocator2</b> interface enables the network provider to determine the physical channel, transport stream ID, and program number of an ATSC transmission.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IATSCLocator2</b> interface inherits from <a href="https://msdn.microsoft.com/8ca7d50f-e7cc-4938-a2ed-fce5278b73fd">IATSCLocator</a>. <b>IATSCLocator2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IATSCLocator2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66f92cb0-a89e-4c34-8995-a94eb1bc33dc">get_ProgramNumber</a>
</td>
<td align="left" width="63%">
Retrieves the program number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af4eeac6-4eee-41d7-a35d-439e4143f046">put_ProgramNumber</a>
</td>
<td align="left" width="63%">
Specifies the program number.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IATSCLocator2)</code>.




## -see-also




<a href="https://msdn.microsoft.com/8ca7d50f-e7cc-4938-a2ed-fce5278b73fd">IATSCLocator</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

