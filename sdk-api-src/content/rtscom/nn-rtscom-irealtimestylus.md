---
UID: NN:rtscom.IRealTimeStylus
title: IRealTimeStylus (rtscom.h)
description: Handles the stylus packet data from a digitizer in real time.
helpviewer_keywords: ["IRealTimeStylus","IRealTimeStylus interface [Tablet PC]","IRealTimeStylus interface [Tablet PC]","described","bfd13012-decf-423a-bc1a-39fb9b0eb64e","rtscom/IRealTimeStylus","tablet.irealtimestylus"]
old-location: tablet\irealtimestylus.htm
tech.root: tablet
ms.assetid: bfd13012-decf-423a-bc1a-39fb9b0eb64e
ms.date: 12/05/2018
ms.keywords: IRealTimeStylus, IRealTimeStylus interface [Tablet PC], IRealTimeStylus interface [Tablet PC],described, bfd13012-decf-423a-bc1a-39fb9b0eb64e, rtscom/IRealTimeStylus, tablet.irealtimestylus
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
req.lib: 
req.dll: RTSCom.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRealTimeStylus
 - rtscom/IRealTimeStylus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IRealTimeStylus
---

# IRealTimeStylus interface


## -description

Handles the stylus packet data from a digitizer in real time.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRealTimeStylus</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRealTimeStylus</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-addcustomstylusdatatoqueue">AddCustomStylusDataToQueue</a>
</td>
<td align="left" width="63%">
Adds custom data to the specified queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-addstylusasyncplugin">AddStylusAsyncPlugin</a>
</td>
<td align="left" width="63%">
Adds an <a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a> to the asynchronous plug-in collection at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-addstylussyncplugin">AddStylusSyncPlugin</a>
</td>
<td align="left" width="63%">
Adds an <a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a> to the synchronous plug-in collection at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-clearstylusqueues">ClearStylusQueues</a>
</td>
<td align="left" width="63%">
Clears both the input and the output queues of data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-getalltabletcontextids">GetAllTabletContextIds</a>
</td>
<td align="left" width="63%">
Retrieves an array of <b>TABLET_CONTEXT_ID</b>s.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-getdesiredpacketdescription">GetDesiredPacketDescription</a>
</td>
<td align="left" width="63%">
Retrieves the properties that are requested to be included in the packet stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-getpacketdescriptiondata">GetPacketDescriptionData</a>
</td>
<td align="left" width="63%">
Retrieves the actual properties that will be received from the hardware based on the request made by the call to <a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-setdesiredpacketdescription">IRealTimeStylus::SetDesiredPacketDescription Method</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-getstylusasyncplugin">GetStylusAsyncPlugin</a>
</td>
<td align="left" width="63%">
Retrieves the plug-in at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-getstylusasyncplugincount">GetStylusAsyncPluginCount</a>
</td>
<td align="left" width="63%">
Gets the count of plug-ins in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-getstyluses">GetStyluses</a>
</td>
<td align="left" width="63%">
Retrieves the collection of styluses this instance of the <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object has encountered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-getstylusforid">GetStylusForId</a>
</td>
<td align="left" width="63%">
Retrieves a stylus for the specific stylus identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-getstylussyncplugin">GetStylusSyncPlugin</a>
</td>
<td align="left" width="63%">
Retrieves the plug-in at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-getstylussyncplugincount">GetStylusSyncPluginCount</a>
</td>
<td align="left" width="63%">
Gets the count of plug-ins in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-gettablet">GetTablet</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet Interface</a> object to the caller.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-gettabletcontextidfromtablet">GetTabletContextIdFromTablet</a>
</td>
<td align="left" width="63%">
Retrieves the <b>TABLET_CONTEXT_ID</b> for a specific tablet.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-gettabletfromtabletcontextid">GetTabletFromTabletContextId</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet Interface</a> for a specific tablet context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-removeallstylusasyncplugins">RemoveAllStylusAsyncPlugins</a>
</td>
<td align="left" width="63%">
Removes all the plug-ins from the asynchronous plug-in collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-removeallstylussyncplugins">RemoveAllStylusSyncPlugins</a>
</td>
<td align="left" width="63%">
Removes all the plug-ins from the synchronous plug-in collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-removestylusasyncplugin">RemoveStylusAsyncPlugin</a>
</td>
<td align="left" width="63%">
Removes and retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a> from the collection at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-removestylussyncplugin">RemoveStylusSyncPlugin</a>
</td>
<td align="left" width="63%">
Removes and optionally retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a> from the collection at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-setalltabletsmode">SetAllTabletsMode</a>
</td>
<td align="left" width="63%">
Sets the mode for the <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus</a> to forward packets from all attached tablets.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-setdesiredpacketdescription">SetDesiredPacketDescription</a>
</td>
<td align="left" width="63%">
Requests which properties should be included in the packet stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-setsingletabletmode">SetSingleTabletMode</a>
</td>
<td align="left" width="63%">
Sets the mode for the <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus</a> to forward packets from a single attached tablet.

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

<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-get_childrealtimestylusplugin">ChildRealTimeStylusPlugin</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Enables the developer to add a <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object as an asynchronous plug-in of the current <b>RealTimeStylus Class</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-get_enabled">Enabled</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-get_hwnd">HWND</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the window handle associated with this <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-get_windowinputrectangle">WindowInputRectangle</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the window input rectangle for the <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object.

</td>
</tr>
</table>

## -remarks

This interface is implemented by the <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>.

Extensibility is provided through synchronous and asynchronous plug-in models, using the <a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a> and <a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a> interfaces respectively to conduct custom processing. Use asynchronous plug-ins for computationally intense operations to avoid blocking the packet stream.

We recommend that you do not use the <a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a> interface implementations for CPU and time-intensive operations since this blocks the packet stream flow. These operations should be conducted in <a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a> interface implementation classes which run on a different thread than the thread that maintains the packet stream flow.

<div class="alert"><b>Note</b>  The synchronous and asynchronous plug-in collections on the <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> can be modified without disabling and then re-enabling the <b>RealTimeStylus Class</b> object.</div>
<div> </div>

## -see-also

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-reference">RealTimeStylus Reference</a>

