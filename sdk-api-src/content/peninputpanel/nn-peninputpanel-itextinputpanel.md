---
UID: NN:peninputpanel.ITextInputPanel
title: ITextInputPanel (peninputpanel.h)

description: Provides control of appearance and behavior of the Tablet PC Input Panel.
old-location: tablet\itextinputpanel.htm
tech.root: tablet
ms.assetid: 1e719900-db58-430d-9059-efb3f884f6f0

ms.date: 12/05/2018
ms.keywords: 1e719900-db58-430d-9059-efb3f884f6f0, ITextInputPanel, ITextInputPanel interface [Tablet PC], ITextInputPanel interface [Tablet PC],described, peninputpanel/ITextInputPanel, tablet.itextinputpanel
ms.topic: interface
f1_keywords: 
 - "peninputpanel/ITextInputPanel"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextInputPanel interface


## -description


<p class="CCE_Message">[<b>ITextInputPanel</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://docs.microsoft.com/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelconfiguration">IInputPanelConfiguration</a>.

]


Provides control of appearance and behavior of the Tablet PC Input Panel.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextInputPanel</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITextInputPanel</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-advise">Advise</a>
</td>
<td align="left" width="63%">
Establishes an advisory connection between the Tablet PC Input Panel and the specified sink object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-commitpendinginput">CommitPendingInput</a>
</td>
<td align="left" width="63%">
Sends collected ink to the recognizer and posts the recognition result.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-setinplacehovertargetposition">SetInPlaceHoverTargetPosition</a>
</td>
<td align="left" width="63%">
Explicitly positions the Tablet PC Input Panel hover target in screen coordinates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-setinplaceposition">SetInPlacePosition</a>
</td>
<td align="left" width="63%">
Explicitly positions the Tablet PC Input Panel in screen coordinates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-setinplacevisibility">SetInPlaceVisibility</a>
</td>
<td align="left" width="63%">
Shows or hides the Tablet PC Input Panel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-unadvise">Unadvise</a>
</td>
<td align="left" width="63%">
Terminates an advisory connection previously established through the <a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-advise">ITextInputPanel::Advise Method</a>.

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

<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_attachededitwindow">AttachedEditWindow</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_currentcorrectionmode">CurrentCorrectionMode</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the current correction comb mode as specified by the <a href="https://docs.microsoft.com/windows/win32/api/peninputpanel/ne-peninputpanel-correctionmode">CorrectionMode Enumeration</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_currentinplacestate">CurrentInPlaceState</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the current in-place state as specified by the <a href="https://docs.microsoft.com/windows/win32/api/peninputpanel/ne-peninputpanel-inplacestate">InPlaceState Enumeration</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_currentinputarea">CurrentInputArea</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the current input area as specified by the <a href="https://docs.microsoft.com/windows/win32/api/peninputpanel/ne-peninputpanel-panelinputarea">PanelInputArea Enumeration</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_currentinteractionmode">CurrentInteractionMode</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the positioning of the Tablet PC Input Panel as specified by the <a href="https://docs.microsoft.com/windows/win32/api/peninputpanel/ne-peninputpanel-interactionmode">InteractionMode Enumeration</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_defaultinplacestate">DefaultInPlaceState</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the default in-place state as specified by the <a href="https://docs.microsoft.com/windows/win32/api/peninputpanel/ne-peninputpanel-inplacestate">InPlaceState Enumeration</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_defaultinputarea">DefaultInputArea</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the default input area as specified by the <a href="https://docs.microsoft.com/windows/win32/api/peninputpanel/ne-peninputpanel-panelinputarea">PanelInputArea Enumeration</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_expandpostinsertioncorrection">ExpandPostInsertionCorrection</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_inplaceboundingrectangle">InPlaceBoundingRectangle</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_inplacevisibleonfocus">InPlaceVisibleOnFocus</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_popdowncorrectionheight">PopDownCorrectionHeight</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_popupcorrectionheight">PopUpCorrectionHeight</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_preferredinplacedirection">PreferredInPlaceDirection</a>


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



<b>ITextInputPanel Interface</b> gives application developers more control and information about Input Panel's state than <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel Class</a>. <b>ITextInputPanel Interface</b> replaces the <b>PenInputPanel Class</b> as the preferred mechanism for programmatically interacting with the Input Panel.

<b>ITextInputPanel Interface</b> provides:

<ul>
<li>A complete control over the positioning of the in-place Input Panel when the application has focus.</li>
<li>An access to the ink objects from the Input Panel text insertion in addition to the recognized text.</li>
<li>A set of properties that correspond exactly to Input Panel's capabilities giving both the ability to know Input Panel's current state and to customize Input Panel's configuration.</li>
</ul>
The <b>ITextInputPanel Interface</b> continues to provide nearly all of the programmatic capabilities of the <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel Class</a> thus superseding the <b>PenInputPanel Class</b>.

This element is declared in Peninputpanel.h.



