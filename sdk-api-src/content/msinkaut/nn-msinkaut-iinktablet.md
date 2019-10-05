---
UID: NN:msinkaut.IInkTablet
title: IInkTablet (msinkaut.h)
author: windows-sdk-content
description: Represents the digitizer device of Tablet PC that receives tablet device messages or events.
old-location: tablet\iinktablet.htm
tech.root: tablet
ms.assetid: 9a945740-b191-41f5-8b3d-49b7e2d1e463
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 9a945740-b191-41f5-8b3d-49b7e2d1e463, IInkTablet, IInkTablet interface [Tablet PC], IInkTablet interface [Tablet PC],described, msinkaut/IInkTablet, tablet.iinktablet
ms.topic: interface
f1_keywords: 
 - "msinkaut/IInkTablet"
dev_langs:
 - c++
req.header: msinkaut.h
req.include-header: 
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkTablet interface


## -description



Represents the digitizer device of Tablet PC that receives tablet device messages or events.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkTablet</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkTablet</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics">GetPropertyMetrics</a>
</td>
<td align="left" width="63%">
Returns the metrics data for a known property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-ispacketpropertysupported">IsPacketPropertySupported</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-get_hardwarecapabilities">HardwareCapabilities</a>


</td>
<td align="left" width="63%">
Gets a value from the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/ne-msinkaut-tablethardwarecapabilities">TabletHardwareCapabilities</a> enumeration that defines the hardware capabilities of the <b>IInkTablet</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-get_maximuminputrectangle">MaximumInputRectangle</a>


</td>
<td align="left" width="63%">
Gets the maximum input rectangle, in tablet device coordinates that the <b>IInkTablet</b> object supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-get_name">Name</a>


</td>
<td align="left" width="63%">
Gets the name of the <b>IInkTablet</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-get_plugandplayid">PlugAndPlayID</a>


</td>
<td align="left" width="63%">
Gets a string representation of the Plug and Play identifier of the <b>IInkTablet</b> object.

</td>
</tr>
</table> 


## -remarks



You can use the <b>IInkTablet</b> object to determine the hardware capabilities of the tablet device. A Tablet PC may have more than one digitizer attached in addition to the built-in digitizer.

<b>IInkTablet</b> objects work closely with ink collector objects. An ink collector (<a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-class">InkCollector</a>, <a href="https://docs.microsoft.com/windows/desktop/tablet/inkoverlay-class">InkOverlay</a>, or <a href="https://docs.microsoft.com/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a>) can be set to one of two tablet-related modes:

<ul>
<li>All tablets mode</li>
<li>Single tablet integrated mode</li>
</ul>
The default mode is all tablets mode (set with the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setalltabletsmode">SetAllTabletsMode</a> method of the ink collector). This mode integrates all tablet devices if multiple devices are attached to the Tablet PC. Because all of the tablets are integrated, available cursors can be used on any of the tablet devices, and each tablet maps to the entire screen. This allows automatic updating of the windows.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor">IInkCursor Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-class">InkCollector Class</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkpicture-control-reference">InkPicture Control Reference</a>
 

 

