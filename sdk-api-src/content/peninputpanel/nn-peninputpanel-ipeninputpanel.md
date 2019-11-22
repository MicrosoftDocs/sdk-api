---
UID: NN:peninputpanel.IPenInputPanel
title: IPenInputPanel (peninputpanel.h)

description: "."
old-location: tablet\ipeninputpanel.htm
tech.root: tablet
ms.assetid: AA973F9D-264F-4D08-9D86-C5DAEF1C09D5

ms.date: 12/05/2018
ms.keywords: IPenInputPanel, IPenInputPanel interface [Tablet PC], IPenInputPanel interface [Tablet PC],described, peninputpanel/IPenInputPanel, tablet.ipeninputpanel
ms.topic: interface
f1_keywords: 
 - "peninputpanel/IPenInputPanel"
dev_langs:
 - c++
req.header: peninputpanel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - peninputpanel.h
api_name:
 - IPenInputPanel
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPenInputPanel interface


## -description





## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPenInputPanel</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPenInputPanel</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Events</a></li>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPenInputPanel</b> interface has these events.
<table class="members" id="memberListEvents">
<tr>
<th align="left" width="37%">Event</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-inputfailed">InputFailed</a>
</td>
<td align="left" width="63%">
Deprecated.  The <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="https://docs.microsoft.com/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.

Occurs when input focus changes before the <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object was able to insert user input into the attached control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-panelchanged">PanelChanged</a>
</td>
<td align="left" width="63%">
Deprecated.  The <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="https://docs.microsoft.com/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.

Occurs when the <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object changes between layouts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-panelmoving">PanelMoving</a>
</td>
<td align="left" width="63%">
Deprecated.  The <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="https://docs.microsoft.com/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.

Occurs when the <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object is moving.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-visiblechanged">VisibleChanged</a>
</td>
<td align="left" width="63%">
Deprecated.  The <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="https://docs.microsoft.com/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.

Occurs when the <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object has shown or hidden itself.

</td>
</tr>
</table> 
<h3><a id="methods"></a>Methods</h3>The <b>IPenInputPanel</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput">CommitPendingInput</a>
</td>
<td align="left" width="63%">
Deprecated.  The <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="https://docs.microsoft.com/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.

Sends collected ink to the recognizer and posts the recognition result.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-enabletsf">EnableTsf</a>
</td>
<td align="left" width="63%">
Deprecated. Gets or sets a Boolean value that indicates whether the <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object attempts to send text to the attached control through the <a href="https://docs.microsoft.com/windows/desktop/TSF/text-services-framework">Text Services Framework</a> (TSF) and enables the use of the <b>correction</b> user interface.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto">MoveTo</a>
</td>
<td align="left" width="63%">
Deprecated.  The <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="https://docs.microsoft.com/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.

Sets the position of the <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object to a static screen position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh">Refresh</a>
</td>
<td align="left" width="63%">

<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh">Refresh</a> is no longer available for use as of Windows XP Tablet PC Edition.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPenInputPanel</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow">AttachedEditWindow</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Deprecated.  The <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="https://docs.microsoft.com/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.

Sets or gets the window handle of the object that the <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object is attached to.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow">AutoShow</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Deprecated.  The <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="https://docs.microsoft.com/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.

Gets or sets a value that indicates whether the pen input panel appears when focus is set on the attached control by using the pen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_busy">Busy</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Deprecated.  The <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="https://docs.microsoft.com/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.

Gets a a value that indicates whether the <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object is currently processing ink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel">CurrentPanel</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Deprecated.  The <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="https://docs.microsoft.com/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.

Gets or sets which panel type is currently being used for input within the <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_defaultpanel">DefaultPanel</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Deprecated.  The <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="https://docs.microsoft.com/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.

Gets or sets the default panel type used for input within the <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid">Factoid</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Deprecated.  The <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="https://docs.microsoft.com/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.

Gets or sets the string name of the factoid used by the <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_height">Height</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Deprecated.  The <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="https://docs.microsoft.com/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.

Gets the height of the pen input panel in client coordinates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_horizontaloffset">HorizontalOffset</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Deprecated.  The <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="https://docs.microsoft.com/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.

Gets or sets the offset between the left edge of the pen input panel and the left edge of the control to which it is attached.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left">Left</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Deprecated.  The <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="https://docs.microsoft.com/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.

Gets the horizontal, or x-axis, location of the left edge of the <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object, in screen coordinates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top">Top</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Deprecated.  The <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="https://docs.microsoft.com/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.

Gets the vertical, or y-axis, location of the top edge of the <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object, in screen coordinates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_verticaloffset">VerticalOffset</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Deprecated.  The <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="https://docs.microsoft.com/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.

Gets or sets the offset between the closest horizontal edge of the pen input panel  and the closest horizontal edge of the control to which it is attached.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_visible">Visible</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Deprecated.  The <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="https://docs.microsoft.com/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.

Gets or sets a value that indicates whether the <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object is visible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_width">Width</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Deprecated.  The <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="https://docs.microsoft.com/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.

Gets the width of the pen input panel  in client coordinates.

</td>
</tr>
</table> 

