---
UID: NN:manipulations.IManipulationProcessor
title: IManipulationProcessor (manipulations.h)
description: The IManipulationProcessor provides functionality for monitoring and responding to multitouch input.helpviewer_keywords: ["IManipulationProcessor","IManipulationProcessor interface [Windows Touch]","IManipulationProcessor interface [Windows Touch]","described","manipulations/IManipulationProcessor","wintouch.imanipulationprocessor"]
old-location: wintouch\imanipulationprocessor.htm
tech.root: wintouch
ms.assetid: 963f87c1-e128-4bd5-9f28-d49418f768fb
ms.date: 12/05/2018
ms.keywords: IManipulationProcessor, IManipulationProcessor interface [Windows Touch], IManipulationProcessor interface [Windows Touch],described, manipulations/IManipulationProcessor, wintouch.imanipulationprocessor
f1_keywords:
- manipulations/IManipulationProcessor
dev_langs:
- c++
req.header: manipulations.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
- manipulations.h
api_name:
- IManipulationProcessor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IManipulationProcessor interface


## -description


The IManipulationProcessor provides functionality for monitoring and responding to multitouch input.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IManipulationProcessor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IManipulationProcessor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IManipulationProcessor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-completemanipulation">CompleteManipulation</a>
</td>
<td align="left" width="63%">
Call this method when you want manipulation to end.  This method raises the <a href="https://docs.microsoft.com/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted">ManipulationCompleted</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getangularvelocity">GetAngularVelocity</a>
</td>
<td align="left" width="63%">
Calculates the rotational velocity that the target object is moving at.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getexpansionvelocity">GetExpansionVelocity</a>
</td>
<td align="left" width="63%">
Calculates the rate that the target object is expanding at.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getvelocityx">GetVelocityX</a>
</td>
<td align="left" width="63%">
Calculates and returns the horizontal velocity for the target object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getvelocityy">GetVelocityY</a>
</td>
<td align="left" width="63%">
Calculates and returns the vertical velocity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdown">ProcessDown</a>
</td>
<td align="left" width="63%">
Feeds data to the manipulation processor associated with a target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime">ProcessDownWithTime</a>
</td>
<td align="left" width="63%">
Feeds data including a timestamp to the manipulation processor associated with a target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmove">ProcessMove</a>
</td>
<td align="left" width="63%">
Feeds data to the manipulation processor associated with a target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime">ProcessMoveWithTime</a>
</td>
<td align="left" width="63%">
Feeds data including a timestamp to the manipulation processor associated with a target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processup">ProcessUp</a>
</td>
<td align="left" width="63%">
Feeds data to the manipulation processor associated with a target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime">ProcessUpWithTime</a>
</td>
<td align="left" width="63%">
Feeds data including a timestamp to the manipulation processor associated with a target.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IManipulationProcessor</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/wintouch/imanipulationprocessor-minimumscalerotateradius">MinimumScaleRotateRadius</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies how large the distance contacts on a scale or rotate gesture need to be to trigger manipulation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx">PivotPointX</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
This property is the horizontal center of the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy">PivotPointY</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
This property is the vertical center of the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius">PivotRadius</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
This property is used to determine how much rotation is used in single finger manipulation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_supportedmanipulations">SupportedManipulations</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
This property is used to indicate which manipulations are supported by an object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wintouch/intertmanip-classes-and-interfaces">Classes and Interfaces</a>
 

 

