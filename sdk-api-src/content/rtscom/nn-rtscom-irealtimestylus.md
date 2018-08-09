---
UID: NN:rtscom.IRealTimeStylus
title: IRealTimeStylus
author: windows-sdk-content
description: Handles the stylus packet data from a digitizer in real time.
old-location: tablet\irealtimestylus.htm
old-project: tablet
ms.assetid: bfd13012-decf-423a-bc1a-39fb9b0eb64e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IRealTimeStylus, IRealTimeStylus interface [Tablet PC], IRealTimeStylus interface [Tablet PC],described, bfd13012-decf-423a-bc1a-39fb9b0eb64e, rtscom/IRealTimeStylus, tablet.irealtimestylus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: rtscom.h
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
tech.root: 
req.typenames: StylusQueue
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IRealTimeStylus
product: Windows
targetos: Windows
req.lib: 
req.dll: RTSCom.dll
req.irql: 
req.product: ADAM
---

# IRealTimeStylus interface


## -description



Handles the stylus packet data from a digitizer in real time.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRealTimeStylus</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRealTimeStylus</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IRealTimeStylus</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d216853-9103-4027-a724-f35d84553a9b">AddCustomStylusDataToQueue</a>
</td>
<td align="left" width="63%">
Adds custom data to the specified queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc22fa79-469a-47f0-96ce-9a041fc8a617">AddStylusAsyncPlugin</a>
</td>
<td align="left" width="63%">
Adds an <a href="https://msdn.microsoft.com/bf961d70-2576-493b-a34d-c7c72b6c0234">IStylusAsyncPlugin</a> to the asynchronous plug-in collection at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db38e39a-27ba-42ca-8748-b5e9c4db18f7">AddStylusSyncPlugin</a>
</td>
<td align="left" width="63%">
Adds an <a href="https://msdn.microsoft.com/e3e02d5a-a004-49de-b2d8-86ccfc120481">IStylusSyncPlugin</a> to the synchronous plug-in collection at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/28270403-9d6d-4e57-9ec5-0d697f4df185">ClearStylusQueues</a>
</td>
<td align="left" width="63%">
Clears both the input and the output queues of data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1fac0624-2e1c-44b2-8a11-82b746a18356">GetAllTabletContextIds</a>
</td>
<td align="left" width="63%">
Retrieves an array of <b>TABLET_CONTEXT_ID</b>s.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8799eb17-8ad0-49c1-a278-40b3bff9d281">GetDesiredPacketDescription</a>
</td>
<td align="left" width="63%">
Retrieves the properties that are requested to be included in the packet stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7eff81c6-8ed5-434b-8e78-fcdb952f37e8">GetPacketDescriptionData</a>
</td>
<td align="left" width="63%">
Retrieves the actual properties that will be received from the hardware based on the request made by the call to <a href="https://msdn.microsoft.com/1ea8359b-fc9f-4929-9499-c5017eb3d763">IRealTimeStylus::SetDesiredPacketDescription Method</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/229e14f6-e0b1-40e0-a58e-daf1ba08cd1f">GetStylusAsyncPlugin</a>
</td>
<td align="left" width="63%">
Retrieves the plug-in at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45861b92-0a2c-42ec-96e5-c3afd45e0e85">GetStylusAsyncPluginCount</a>
</td>
<td align="left" width="63%">
Gets the count of plug-ins in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e838591-ce9e-4f3f-9b5e-b8414faac6ba">GetStyluses</a>
</td>
<td align="left" width="63%">
Retrieves the collection of styluses this instance of the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object has encountered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16218bd3-9e92-407b-99b1-155d4387641e">GetStylusForId</a>
</td>
<td align="left" width="63%">
Retrieves a stylus for the specific stylus identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec587954-cf7c-4f2d-a20d-b401011f7140">GetStylusSyncPlugin</a>
</td>
<td align="left" width="63%">
Retrieves the plug-in at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f8d9097-6f17-4c62-a624-98583ac26f98">GetStylusSyncPluginCount</a>
</td>
<td align="left" width="63%">
Gets the count of plug-ins in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38970fc0-ec4c-4068-a146-83edaa040c8c">GetTablet</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet Interface</a> object to the caller.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f4cc882-c25f-4862-8b78-4db108d0b5d4">GetTabletContextIdFromTablet</a>
</td>
<td align="left" width="63%">
Retrieves the <b>TABLET_CONTEXT_ID</b> for a specific tablet.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be736eaf-8632-4e71-b1d8-c851a9d417e5">GetTabletFromTabletContextId</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet Interface</a> for a specific tablet context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98b97156-f181-45f4-9cfb-13816f8042e6">RemoveAllStylusAsyncPlugins</a>
</td>
<td align="left" width="63%">
Removes all the plug-ins from the asynchronous plug-in collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d6aa14b-f1f5-460a-b37a-5187022ad301">RemoveAllStylusSyncPlugins</a>
</td>
<td align="left" width="63%">
Removes all the plug-ins from the synchronous plug-in collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c993147-3711-45ad-8996-e1434fd4b657">RemoveStylusAsyncPlugin</a>
</td>
<td align="left" width="63%">
Removes and retrieves an <a href="https://msdn.microsoft.com/bf961d70-2576-493b-a34d-c7c72b6c0234">IStylusAsyncPlugin</a> from the collection at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f04dc8a-c0f5-47fd-a814-490e1dfe2cf8">RemoveStylusSyncPlugin</a>
</td>
<td align="left" width="63%">
Removes and optionally retrieves an <a href="https://msdn.microsoft.com/e3e02d5a-a004-49de-b2d8-86ccfc120481">IStylusSyncPlugin</a> from the collection at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb8b2a17-68b9-482b-b212-ad129522ff2e">SetAllTabletsMode</a>
</td>
<td align="left" width="63%">
Sets the mode for the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus</a> to forward packets from all attached tablets.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ea8359b-fc9f-4929-9499-c5017eb3d763">SetDesiredPacketDescription</a>
</td>
<td align="left" width="63%">
Requests which properties should be included in the packet stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f3645fd-cb1e-4bd5-a995-d70197c61afc">SetSingleTabletMode</a>
</td>
<td align="left" width="63%">
Sets the mode for the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus</a> to forward packets from a single attached tablet.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRealTimeStylus</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/269c133c-6950-40e0-8de9-e38bfa06995e">ChildRealTimeStylusPlugin</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Enables the developer to add a <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object as an asynchronous plug-in of the current <b>RealTimeStylus Class</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn966102">Enabled</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Enables or disables the collection of stylus data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b6bc8053-80fa-45f3-8096-272b471a5f6d">HWND</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the window handle associated with this <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e202be43-48c7-4fa4-b049-efdda3ef2ada">WindowInputRectangle</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the window input rectangle for the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object.

</td>
</tr>
</table> 


## -remarks



This interface is implemented by the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a>.

Extensibility is provided through synchronous and asynchronous plug-in models, using the <a href="https://msdn.microsoft.com/e3e02d5a-a004-49de-b2d8-86ccfc120481">IStylusSyncPlugin</a> and <a href="https://msdn.microsoft.com/bf961d70-2576-493b-a34d-c7c72b6c0234">IStylusAsyncPlugin</a> interfaces respectively to conduct custom processing. Use asynchronous plug-ins for computationally intense operations to avoid blocking the packet stream.

We recommend that you do not use the <a href="https://msdn.microsoft.com/e3e02d5a-a004-49de-b2d8-86ccfc120481">IStylusSyncPlugin</a> interface implementations for CPU and time-intensive operations since this blocks the packet stream flow. These operations should be conducted in <a href="https://msdn.microsoft.com/bf961d70-2576-493b-a34d-c7c72b6c0234">IStylusAsyncPlugin</a> interface implementation classes which run on a different thread than the thread that maintains the packet stream flow.

<div class="alert"><b>Note</b>  The synchronous and asynchronous plug-in collections on the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> can be modified without disabling and then re-enabling the <b>RealTimeStylus Class</b> object.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a>



<a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a>



<a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>



<a href="https://msdn.microsoft.com/a239b53c-7fc9-4211-962a-6cfbe0be4e4c">RealTimeStylus Reference</a>
 

 

