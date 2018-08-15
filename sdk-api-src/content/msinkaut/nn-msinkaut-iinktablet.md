---
UID: NN:msinkaut.IInkTablet
title: IInkTablet
author: windows-sdk-content
description: Represents the digitizer device of Tablet PC that receives tablet device messages or events.
old-location: tablet\iinktablet.htm
old-project: tablet
ms.assetid: 9a945740-b191-41f5-8b3d-49b7e2d1e463
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 9a945740-b191-41f5-8b3d-49b7e2d1e463, IInkTablet, IInkTablet interface [Tablet PC], IInkTablet interface [Tablet PC],described, msinkaut/IInkTablet, tablet.iinktablet
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msinkaut.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TabletPropertyMetricUnit
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkTablet
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkTablet interface


## -description



Represents the digitizer device of Tablet PC that receives tablet device messages or events.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkTablet</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInkTablet</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IInkTablet</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9656bb56-01aa-4e9b-a3ad-4fbf117cdfeb">GetPropertyMetrics</a>
</td>
<td align="left" width="63%">
Returns the metrics data for a known property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4bf2e2b0-d45a-4392-990e-5e9320333c0b">IsPacketPropertySupported</a>
</td>
<td align="left" width="63%">
Determines whether a property of a tablet device, identified with a globally unique identifier (GUID), is supported.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkTablet</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/886c1e7c-fec0-4294-aba1-8e0806c2d0ca">HardwareCapabilities</a>


</td>
<td align="left" width="63%">
Gets a value from the <a href="https://msdn.microsoft.com/ab8dfca3-df5e-40a7-9da2-d19447bc746b">TabletHardwareCapabilities</a> enumeration that defines the hardware capabilities of the <b>IInkTablet</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/84d8518b-6cd7-4da9-9ce3-1ce6fe6eeb43">MaximumInputRectangle</a>


</td>
<td align="left" width="63%">
Gets the maximum input rectangle, in tablet device coordinates that the <b>IInkTablet</b> object supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8388ca02-b464-47e4-9911-1c55ce398557">Name</a>


</td>
<td align="left" width="63%">
Gets the name of the <b>IInkTablet</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5b33bd06-fee3-41b0-b3c1-d16b43685c60">PlugAndPlayID</a>


</td>
<td align="left" width="63%">
Gets a string representation of the Plug and Play identifier of the <b>IInkTablet</b> object.

</td>
</tr>
</table> 


## -remarks



You can use the <b>IInkTablet</b> object to determine the hardware capabilities of the tablet device. A Tablet PC may have more than one digitizer attached in addition to the built-in digitizer.

<b>IInkTablet</b> objects work closely with ink collector objects. An ink collector (<a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a>, <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a>, or <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a>) can be set to one of two tablet-related modes:

<ul>
<li>All tablets mode</li>
<li>Single tablet integrated mode</li>
</ul>
The default mode is all tablets mode (set with the <a href="https://msdn.microsoft.com/cb41bc4c-c8fe-4cd6-8049-8cb44a2716a8">SetAllTabletsMode</a> method of the ink collector). This mode integrates all tablet devices if multiple devices are attached to the Tablet PC. Because all of the tablets are integrated, available cursors can be used on any of the tablet devices, and each tablet maps to the entire screen. This allows automatic updating of the windows.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).




## -see-also




<a href="https://msdn.microsoft.com/39b365ad-1eb0-4183-8799-a3c3ecbd3f6e">IInkCursor Interface</a>



<a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector Class</a>



<a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay Class</a>



<a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture Control Reference</a>
 

 

