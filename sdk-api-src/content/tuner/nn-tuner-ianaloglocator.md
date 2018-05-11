---
UID: NN:tuner.IAnalogLocator
title: IAnalogLocator
author: windows-driver-content
description: The IAnalogLocator interface provides tuning information for an analog television network.
old-location: mstv\ianaloglocator.htm
old-project: mstv
ms.assetid: d5ed0dcc-347d-4196-a551-88775cb1b253
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IAnalogLocator, IAnalogLocator interface [Microsoft TV Technologies], IAnalogLocator interface [Microsoft TV Technologies],described, IAnalogLocatorInterface, mstv.ianaloglocator, tuner/IAnalogLocator
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IAnalogLocator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IAnalogLocator interface


## -description



The <b>IAnalogLocator</b> interface provides tuning information for an analog television network.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAnalogLocator</b> interface inherits from <a href="https://msdn.microsoft.com/1d6c18f0-e7f1-4a1c-9edb-e4b66297becf">ILocator</a>. <b>IAnalogLocator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAnalogLocator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8530f436-8067-43bd-8f64-45e042ccb466">get_VideoStandard</a>
</td>
<td align="left" width="63%">
Retrieves the format of the analog television signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6af47a98-ceea-45dd-8a34-3f82ed8a66b1">put_VideoStandard</a>
</td>
<td align="left" width="63%">
Specifies the format of the analog television signal.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IAnalogLocator)</code>.




## -see-also




<a href="https://msdn.microsoft.com/1d6c18f0-e7f1-4a1c-9edb-e4b66297becf">ILocator</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

