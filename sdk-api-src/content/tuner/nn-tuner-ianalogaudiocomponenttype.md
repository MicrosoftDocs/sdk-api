---
UID: NN:tuner.IAnalogAudioComponentType
title: IAnalogAudioComponentType
author: windows-sdk-content
description: The IAnalogAudioComponentType interface provides methods for accessing the analog audio mode.
old-location: mstv\ianalogaudiocomponenttype.htm
old-project: mstv
ms.assetid: bd2256b4-6e9a-4520-8988-d271fb2b84af
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IAnalogAudioComponentType, IAnalogAudioComponentType interface [Microsoft TV Technologies], IAnalogAudioComponentType interface [Microsoft TV Technologies],described, IAnalogAudioComponentTypeInterface, mstv.ianalogaudiocomponenttype, tuner/IAnalogAudioComponentType
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IAnalogAudioComponentType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IAnalogAudioComponentType interface


## -description



The <b>IAnalogAudioComponentType</b> interface provides methods for accessing the analog audio mode.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAnalogAudioComponentType</b> interface inherits from <a href="https://msdn.microsoft.com/e83bbbbe-64a9-4ed3-9c32-925ca80c2c38">IComponentType</a>. <b>IAnalogAudioComponentType</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAnalogAudioComponentType</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63c5f2a0-5524-4df0-bc0d-fcd7c6b36167">get_AnalogAudioMode</a>
</td>
<td align="left" width="63%">
Retrieves the analog audio mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb3c4db6-8364-4c95-82d5-62276f26c7bb">put_AnalogAudioMode</a>
</td>
<td align="left" width="63%">
Specifies the analog audio mode.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IAnalogAudioComponentType)</code>.




## -see-also




<a href="https://msdn.microsoft.com/e83bbbbe-64a9-4ed3-9c32-925ca80c2c38">IComponentType</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

