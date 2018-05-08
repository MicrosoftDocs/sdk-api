---
UID: NN:segment.IMSVidInputDevice
title: IMSVidInputDevice
author: windows-driver-content
description: The IMSVidInputDevice interface represents any input device that is recognized by the Video Control, such as a television tuner card.
old-location: mstv\imsvidinputdevice.htm
old-project: mstv
ms.assetid: 5b413ade-4ab2-45fa-98b2-fd93c8f89a43
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IMSVidInputDevice, IMSVidInputDevice interface [Microsoft TV Technologies], IMSVidInputDevice interface [Microsoft TV Technologies],described, IMSVidInputDeviceInterface, mstv.imsvidinputdevice, segment/IMSVidInputDevice
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
-	IMSVidInputDevice
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidInputDevice interface


## -description



The <b>IMSVidInputDevice</b> interface represents any input device that is recognized by the Video Control, such as a television tuner card. This is a generic interface that serves as an abstract base class for input devices. Several interfaces inherit <b>IMSVidInputDevice</b>, including the following:

<ul>
<li>
<a href="https://msdn.microsoft.com/b11f3ac4-c351-4017-9801-98d8edec7449">IMSVidTuner</a>
</li>
<li>
<a href="https://msdn.microsoft.com/640143d3-6712-4e92-a1d9-0689637b3d90">IMSVidAnalogTuner</a>
</li>
</ul>
When a method returns an <b>IMSVidInputDevice</b> pointer, the object that is returned typically supports one of the derived interfaces.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidInputDevice</b> interface inherits from <a href="https://msdn.microsoft.com/5ec85d18-2fed-4fd0-ab94-72d1d4f3f7ef">IMSVidDevice</a>. <b>IMSVidInputDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidInputDevice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f62bcc4-8c58-4663-9b1f-a5ed7d000a79">IsViewable</a>
</td>
<td align="left" width="63%">
Determines whether this device can view the specified tune request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927297">View</a>
</td>
<td align="left" width="63%">
Configures the input device to view the specified tune request.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidInputDevice)</code>.




## -see-also




<a href="https://msdn.microsoft.com/5ec85d18-2fed-4fd0-ab94-72d1d4f3f7ef">IMSVidDevice</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

