---
UID: NN:segment.IMSVidTuner
title: IMSVidTuner
author: windows-driver-content
description: The IMSVidTuner interface manages tuning devices.
old-location: mstv\imsvidtuner.htm
old-project: mstv
ms.assetid: b11f3ac4-c351-4017-9801-98d8edec7449
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IMSVidTuner, IMSVidTuner interface [Microsoft TV Technologies], IMSVidTuner interface [Microsoft TV Technologies], described, IMSVidTunerInterface, mstv.imsvidtuner, segment/IMSVidTuner
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidTuner
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidTuner interface


## -description



The <b>IMSVidTuner</b> interface manages tuning devices. It is exposed by the <a href="https://msdn.microsoft.com/a29f2bb1-650e-43f8-8949-b3944c54a9e1">MSVidBDATunerDevice</a> object, which represents Broadcast Driver Architecture (BDA)-compliant tuning devices. Non-BDA analog tuners expose the <a href="https://msdn.microsoft.com/640143d3-6712-4e92-a1d9-0689637b3d90">IMSVidAnalogTuner</a> interface, which inherits from this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidTuner</b> interface inherits from <a href="https://msdn.microsoft.com/cbc687b1-826d-4738-8d0a-a7b90f5ff20d">IMSVidVideoInputDevice</a>. <b>IMSVidTuner</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidTuner</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/189c878d-bf14-4464-96ce-5d2e09118dc4">get_Tune</a>
</td>
<td align="left" width="63%">
Retrieves the current tune request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d46e7d8a-5111-4737-897b-9e1357e3249a">get_TuningSpace</a>
</td>
<td align="left" width="63%">
Retrieves the current tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31139b6f-aad9-495b-9e8c-39026c8e81a9">put_Tune</a>
</td>
<td align="left" width="63%">
Specifies the tune request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b1da0078-0c5e-439e-9419-670e9e0f812c">put_TuningSpace</a>
</td>
<td align="left" width="63%">
Specifies the tuning space.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidTuner)</code>.




## -see-also




<a href="https://msdn.microsoft.com/cbc687b1-826d-4738-8d0a-a7b90f5ff20d">IMSVidVideoInputDevice</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

