---
UID: NN:peninputpanel.ITextInputPanel
title: ITextInputPanel
author: windows-sdk-content
description: Provides control of appearance and behavior of the Tablet PC Input Panel.
old-location: tablet\itextinputpanel.htm
tech.root: tablet
ms.assetid: 1e719900-db58-430d-9059-efb3f884f6f0
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: 1e719900-db58-430d-9059-efb3f884f6f0, ITextInputPanel, ITextInputPanel interface [Tablet PC], ITextInputPanel interface [Tablet PC],described, peninputpanel/ITextInputPanel, tablet.itextinputpanel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: peninputpanel.h
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
req.dll: Tiptsf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tiptsf.dll
api_name:
 - ITextInputPanel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextInputPanel interface


## -description


<p class="CCE_Message">[<b>ITextInputPanel</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/81E54703-095E-4810-A8A0-2ACBE7F3D634">IInputPanelConfiguration</a>.

]


Provides control of appearance and behavior of the Tablet PC Input Panel.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextInputPanel</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITextInputPanel</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ITextInputPanel</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ea32572-84e6-4230-a634-fc83cb86601f">Advise</a>
</td>
<td align="left" width="63%">
Establishes an advisory connection between the Tablet PC Input Panel and the specified sink object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/652df9e7-5bac-4dc7-bd1a-3934a2bdeb94">CommitPendingInput</a>
</td>
<td align="left" width="63%">
Sends collected ink to the recognizer and posts the recognition result.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f007a76-8499-4128-8525-0498ddeb7300">SetInPlaceHoverTargetPosition</a>
</td>
<td align="left" width="63%">
Explicitly positions the Tablet PC Input Panel hover target in screen coordinates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49bb1a89-7064-4822-866f-739434043869">SetInPlacePosition</a>
</td>
<td align="left" width="63%">
Explicitly positions the Tablet PC Input Panel in screen coordinates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e503857-9276-4308-b4ad-83db25866689">SetInPlaceVisibility</a>
</td>
<td align="left" width="63%">
Shows or hides the Tablet PC Input Panel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ea2c112-0d57-4da6-89da-5afe57ff2346">Unadvise</a>
</td>
<td align="left" width="63%">
Terminates an advisory connection previously established through the <a href="https://msdn.microsoft.com/4ea32572-84e6-4230-a634-fc83cb86601f">ITextInputPanel::Advise Method</a>.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextInputPanel</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/92a8510d-c8f2-44b4-8812-789ddbc0e3fd">AttachedEditWindow</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or gets the window handle of the object to which the <b>ITextInputPanel</b> object is attached.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/92cd44a0-4dc6-4882-9ebb-45aa5b3fbc69">CurrentCorrectionMode</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the current correction comb mode as specified by the <a href="https://msdn.microsoft.com/133d2012-e43c-490a-b126-b7670ea7acf8">CorrectionMode Enumeration</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3ca27156-ed34-4cac-ba26-edded586272a">CurrentInPlaceState</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the current in-place state as specified by the <a href="https://msdn.microsoft.com/95642cbf-4520-44cc-95ba-80de1fe3b447">InPlaceState Enumeration</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/47ffdda4-bfe2-4ee0-bfda-cad73a346b1e">CurrentInputArea</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the current input area as specified by the <a href="https://msdn.microsoft.com/fc262f07-aa73-49c8-a26a-1f0a47f8269a">PanelInputArea Enumeration</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/dd28dad3-4b04-4597-9627-8fd27c75a207">CurrentInteractionMode</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the positioning of the Tablet PC Input Panel as specified by the <a href="https://msdn.microsoft.com/8e01c1fd-3351-47f1-beae-c84d9f7969a8">InteractionMode Enumeration</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/00778a2c-9903-46a0-a5b3-c2ac4c355462">DefaultInPlaceState</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the default in-place state as specified by the <a href="https://msdn.microsoft.com/95642cbf-4520-44cc-95ba-80de1fe3b447">InPlaceState Enumeration</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3e221516-631a-4d15-a9ef-bd05c6928067">DefaultInputArea</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the default input area as specified by the <a href="https://msdn.microsoft.com/fc262f07-aa73-49c8-a26a-1f0a47f8269a">PanelInputArea Enumeration</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/fda9ac46-7aa0-4991-94df-d71772b90726">ExpandPostInsertionCorrection</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that indicates whether the correction comb on the Tablet PC Input Panel is automatically expanded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9a114f9d-b97d-4a2e-ac8e-f0a0241a6fbb">InPlaceBoundingRectangle</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the bounding rectangle for Tablet PC Input Panel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/487ffcee-9df6-48db-8c84-e7e073b8a643">InPlaceVisibleOnFocus</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that indicates whether the Tablet PC Input Panel is displayed automatically when the window to which it is attached gets focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/525e5406-75ff-4f3c-a3f2-a542e04ca203">PopDownCorrectionHeight</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the height of the Post-Insertion correction comb when it is positioned below Input Panel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/986b7527-c634-45d9-a2eb-86fa999e57ba">PopUpCorrectionHeight</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the height of the Post-Insertion correction comb when it is positioned above Input Panel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5d05e315-4e6d-4591-83d8-9cc98f2c2e2b">PreferredInPlaceDirection</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the preferred direction of the in-place Input Panel relative to the text entry field.

</td>
</tr>
</table> 


## -remarks



<b>ITextInputPanel Interface</b> gives application developers more control and information about Input Panel's state than <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel Class</a>. <b>ITextInputPanel Interface</b> replaces the <b>PenInputPanel Class</b> as the preferred mechanism for programmatically interacting with the Input Panel.

<b>ITextInputPanel Interface</b> provides:

<ul>
<li>A complete control over the positioning of the in-place Input Panel when the application has focus.</li>
<li>An access to the ink objects from the Input Panel text insertion in addition to the recognized text.</li>
<li>A set of properties that correspond exactly to Input Panel's capabilities giving both the ability to know Input Panel's current state and to customize Input Panel's configuration.</li>
</ul>
The <b>ITextInputPanel Interface</b> continues to provide nearly all of the programmatic capabilities of the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel Class</a> thus superseding the <b>PenInputPanel Class</b>.

This element is declared in Peninputpanel.h.



