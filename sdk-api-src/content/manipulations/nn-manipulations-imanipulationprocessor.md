---
UID: NN:manipulations.IManipulationProcessor
title: IManipulationProcessor (manipulations.h)
author: windows-sdk-content
description: The IManipulationProcessor provides functionality for monitoring and responding to multitouch input.
old-location: wintouch\imanipulationprocessor.htm
tech.root: wintouch
ms.assetid: 963f87c1-e128-4bd5-9f28-d49418f768fb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IManipulationProcessor, IManipulationProcessor interface [Windows Touch], IManipulationProcessor interface [Windows Touch],described, manipulations/IManipulationProcessor, wintouch.imanipulationprocessor
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IManipulationProcessor interface


## -description


The IManipulationProcessor provides functionality for monitoring and responding to multitouch input.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IManipulationProcessor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IManipulationProcessor</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/01779628-1f46-4cea-90fa-1093e26e0285">CompleteManipulation</a>
</td>
<td align="left" width="63%">
Call this method when you want manipulation to end.  This method raises the <a href="https://msdn.microsoft.com/1284df32-f4e8-43b3-b825-9172ad39f0e6">ManipulationCompleted</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3253837f-c5ea-47f7-ba0a-86e0ed4e228e">GetAngularVelocity</a>
</td>
<td align="left" width="63%">
Calculates the rotational velocity that the target object is moving at.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5dbaeaa3-4abf-485e-9f84-8450dce14fc9">GetExpansionVelocity</a>
</td>
<td align="left" width="63%">
Calculates the rate that the target object is expanding at.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64524f01-f7b2-4e78-97b8-20686018469f">GetVelocityX</a>
</td>
<td align="left" width="63%">
Calculates and returns the horizontal velocity for the target object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b531c4e5-8437-4869-9264-3fe131b8acc8">GetVelocityY</a>
</td>
<td align="left" width="63%">
Calculates and returns the vertical velocity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c192bc4-6922-4c70-961d-1f8684ad792b">ProcessDown</a>
</td>
<td align="left" width="63%">
Feeds data to the manipulation processor associated with a target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a76c9150-49b8-4a74-8ef0-bfa5ce9ec28a">ProcessDownWithTime</a>
</td>
<td align="left" width="63%">
Feeds data including a timestamp to the manipulation processor associated with a target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2c0e975-3edd-43d5-8a58-2d8166413c76">ProcessMove</a>
</td>
<td align="left" width="63%">
Feeds data to the manipulation processor associated with a target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0840ef85-9b18-4248-96fe-93653274a89a">ProcessMoveWithTime</a>
</td>
<td align="left" width="63%">
Feeds data including a timestamp to the manipulation processor associated with a target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c93f6729-5e50-41a1-867c-93e4ce9ecda9">ProcessUp</a>
</td>
<td align="left" width="63%">
Feeds data to the manipulation processor associated with a target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fafea353-9126-454d-9311-4859e5ae5712">ProcessUpWithTime</a>
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

<a href="https://msdn.microsoft.com/b4c49f41-c5ea-4c6a-872b-2d982e588b09">MinimumScaleRotateRadius</a>


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

<a href="https://msdn.microsoft.com/52afdf21-8c5d-4da8-aab2-7a8273df5147">PivotPointX</a>


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

<a href="https://msdn.microsoft.com/09faaacd-3583-4129-b8e3-068e34e220b7">PivotPointY</a>


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

<a href="https://msdn.microsoft.com/793999b6-abb1-4912-9e9c-764f6f68ea29">PivotRadius</a>


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

<a href="https://msdn.microsoft.com/1909394f-83ec-4e13-81af-3e6c70210865">SupportedManipulations</a>


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




<a href="https://msdn.microsoft.com/056bcaa2-580a-457c-a0a6-e01a316dc21a">Classes and Interfaces</a>
 

 

