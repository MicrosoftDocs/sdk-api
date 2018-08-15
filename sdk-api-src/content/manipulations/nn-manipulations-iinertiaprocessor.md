---
UID: NN:manipulations.IInertiaProcessor
title: IInertiaProcessor
author: windows-sdk-content
description: The IInertiaProcessor interface handles calculations regarding object motion for Windows Touch.
old-location: wintouch\iinertiaprocessor.htm
old-project: wintouch
ms.assetid: 8dc171eb-0c6e-41dd-b506-5f91ea703a53
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IInertiaProcessor, IInertiaProcessor interface [Windows Touch], IInertiaProcessor interface [Windows Touch],described, manipulations/IInertiaProcessor, wintouch.iinertiaprocessor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: manipulations.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MANIPULATION_PROCESSOR_MANIPULATIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - manipulations.h
api_name:
 - IInertiaProcessor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IInertiaProcessor interface


## -description


The IInertiaProcessor interface handles calculations regarding object motion for Windows Touch.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInertiaProcessor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInertiaProcessor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IInertiaProcessor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff41789c-afc5-419b-9767-e99572b9b41e">Complete</a>
</td>
<td align="left" width="63%">
Optionally processes the given tick and raises the Completed event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/325e04c2-a477-43c7-9513-36a2a92eef8e">CompleteTime</a>
</td>
<td align="left" width="63%">
Processes the given tick and raises the Completed event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f63cafa0-0da6-46ba-91d3-956dc804dd79">Process</a>
</td>
<td align="left" width="63%">
Performs calculations for the given tick and can raise the <b>Delta</b> or <b>Completed</b> event depending on whether extrapolation is completed or not. If extrapolation finished at the previous tick, the method is no-op.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06132573-e198-4b2c-922b-3eeda53ac10b">ProcessTime</a>
</td>
<td align="left" width="63%">
Performs calculations for the given tick and can raise the <b>Delta</b> or <b>Completed</b> event depending on whether extrapolation is completed or not.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69ce260d-0674-4ff0-8610-bc814976bd3d">Reset</a>
</td>
<td align="left" width="63%">
Initializes the processor with initial time stamp.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInertiaProcessor</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/745d51d2-4d9e-4045-929a-2899ff4d2189">BoundaryBottom</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Limits how far toward the bottom of the screen the target object can move.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/476445bb-bf17-4091-a296-73594bd7ed7f">BoundaryLeft</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Limits how far toward the left of the screen the target object can move.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ff8e0602-4e35-40ad-afae-a03046dda954">BoundaryRight</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Limits how far toward the right of the screen the target object can move.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5864cf0e-c632-414c-a8b1-e8367474e904">BoundaryTop</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Limits how far toward the top of the screen the target object can move.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ee3bb3c8-4d7d-424b-abc9-db7307793794">DesiredAngularDeceleration</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies the desired rate that the target object will stop spinning in radians per msec.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2ad39e7e-b433-4a40-aea2-53cf23247f25">DesiredDeceleration</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies the desired rate at which translation operations will decelerate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cbcd7ce7-7df4-48d8-acfe-dc206f5d70d1">DesiredDisplacement</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies the desired distance that the object will travel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1d686bb1-a00b-43fc-804b-5a1d8bb69499">DesiredExpansion</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies the desired change in the object's average radius.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b21d9aa8-0c86-45fe-9573-023929cf7faa">DesiredExpansionDeceleration</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies the rate at which the object will stop expanding.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/42fcda66-8992-4a44-b4d5-04d4f2c7e25a">DesiredRotation</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies the desired rotation on the current object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8a043ef6-3251-4179-b42f-f59c07287b49">ElasticMarginBottom</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies the lower region for bouncing the target object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3c6925d9-8220-4706-991b-cd0cb5697f29">ElasticMarginLeft</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies the leftmost region for bouncing the target object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/081dd9d4-d190-4a44-bcd8-d5d0d99d7fd2">ElasticMarginRight</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies the rightmost region for bouncing the target object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/76e332bf-180b-466f-8c22-cec4e44a7ab6">ElasticMarginTop</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies the upper boundary for bouncing objects within the elastic region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a15ac600-ef03-4234-ac38-dc3cf212a3cb">InitialAngularVelocity</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies the rotation of the target when movement begins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c0e60b1c-98d0-4b50-ba5d-deda44debf56">InitialExpansionVelocity</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies the rate of radius expansion for a target when the target was affected by inertia.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6c710bd7-6fbe-4bc3-8966-b83d4500625a">InitialOriginX</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or puts the property designating the horizontal position of a target object.  This property specifies the starting horizontal location for a target with inertia.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4b817f8b-79e9-4409-a6b2-2096759bab59">InitialOriginY</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or puts the property designating the vertical location for a target object.  This property specifies the starting vertical location for a target with inertia.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/53179559-e65a-4b5b-b82a-f1fea0cb4509">InitialRadius</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies the distance from the edge of the target to its center before the object was changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7ea7e00f-98f5-4928-9919-705ffa53b91b">InitialTimestamp</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies the starting time stamp for a target object with inertia.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/23ae7083-0a78-4628-8a04-f9bd762aac02">InitialVelocityX</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies the initial movement of the target object on the horizontal axis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3ba0aa0c-a819-4833-883b-218702052ce1">InitialVelocityY</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies the initial movement of the target object on the vertical axis.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/056bcaa2-580a-457c-a0a6-e01a316dc21a">Classes and Interfaces</a>
 

 

