---
UID: NN:richole.IRichEditOle
title: IRichEditOle (richole.h)
description: The IRichEditOle interface exposes the Component Object Model (COM) functionality of a rich edit control. The interface can be obtained by sending the EM_GETOLEINTERFACE message. This interface has the following methods.
helpviewer_keywords: ["IRichEditOle","IRichEditOle interface [Windows Controls]","IRichEditOle interface [Windows Controls]","described","_win32_IRichEditOle","_win32_IRichEditOle_cpp","controls.IRichEditOle","controls._win32_IRichEditOle","richole/IRichEditOle"]
old-location: controls\IRichEditOle.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditole.htm
ms.date: 12/05/2018
ms.keywords: IRichEditOle, IRichEditOle interface [Windows Controls], IRichEditOle interface [Windows Controls],described, _win32_IRichEditOle, _win32_IRichEditOle_cpp, controls.IRichEditOle, controls._win32_IRichEditOle, richole/IRichEditOle
req.header: richole.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRichEditOle
 - richole/IRichEditOle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - IRichEditOle
---

# IRichEditOle interface


## -description

The <b>IRichEditOle</b> interface exposes the Component Object Model (COM) functionality of a rich edit control. The interface can be obtained by sending the <a href="/windows/desktop/Controls/em-getoleinterface">EM_GETOLEINTERFACE</a> message.


This interface has the following methods.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRichEditOle</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRichEditOle</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRichEditOle</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/richole/nf-richole-iricheditole-activateas">ActivateAs</a>
</td>
<td align="left" width="63%">
Handles <a href="/windows/desktop/api/richole/nf-richole-iricheditole-activateas">Activate As</a> behavior by unloading all objects of the old class, telling OLE to treat those objects as objects of the new class, and reloading the objects. If objects cannot be reloaded, they are deleted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/richole/nf-richole-iricheditole-contextsensitivehelp">ContextSensitiveHelp</a>
</td>
<td align="left" width="63%">
Indicates if a rich edit control should transition into or out of context-sensitive help mode. A rich edit control calls the <a href="/windows/desktop/api/richole/nf-richole-iricheditole-contextsensitivehelp">IRichEditOle::ContextSensitiveHelp</a> method of any in-place object which is currently active if a state change is occurring.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/richole/nf-richole-iricheditole-convertobject">ConvertObject</a>
</td>
<td align="left" width="63%">
Converts an object to a new type. This call reloads the object but does not force an update; the caller must do this.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/richole/nf-richole-iricheditole-getclientsite">GetClientSite</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleclientsite">IOleClientSite</a> interface to be used when creating a new object. All objects inserted into a rich edit control must use client site interfaces returned by this function. A client site may be used with exactly one object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/richole/nf-richole-iricheditole-getclipboarddata">GetClipboardData</a>
</td>
<td align="left" width="63%">
Retrieves a clipboard object for a range in an edit control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/richole/nf-richole-iricheditole-getlinkcount">GetLinkCount</a>
</td>
<td align="left" width="63%">
Returns the number of objects in a rich edit control that are links.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/richole/nf-richole-iricheditole-getobject">GetObject</a>
</td>
<td align="left" width="63%">
Retrieves information, stored in a <a href="/windows/desktop/api/richole/ns-richole-reobject">REOBJECT</a> structure, about an object in a rich edit control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/richole/nf-richole-iricheditole-getobjectcount">GetObjectCount</a>
</td>
<td align="left" width="63%">
Returns the number of objects currently contained in a rich edit control. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/richole/nf-richole-iricheditole-handsoffstorage">HandsOffStorage</a>
</td>
<td align="left" width="63%">
Indicates when a rich edit control is to release its reference to the storage interface associated with the specified object. This call does not call the object's <a href="/windows/desktop/api/richole/nf-richole-iricheditole-handsoffstorage">IRichEditOle::HandsOffStorage</a> method; the caller must do that.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/richole/nf-richole-iricheditole-importdataobject">ImportDataObject</a>
</td>
<td align="left" width="63%">
Imports a clipboard object into a rich edit control, replacing the current selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/richole/nf-richole-iricheditole-inplacedeactivate">InPlaceDeactivate</a>
</td>
<td align="left" width="63%">
Indicates when a rich edit control is to deactivate the currently active in-place object, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/richole/nf-richole-iricheditole-insertobject">InsertObject</a>
</td>
<td align="left" width="63%">
Inserts an object into a rich edit control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/richole/nf-richole-iricheditole-savecompleted">SaveCompleted</a>
</td>
<td align="left" width="63%">
Indicates when the most recent save operation has been completed and that the rich edit control should hold onto a different storage for the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/richole/nf-richole-iricheditole-setdvaspect">SetDvaspect</a>
</td>
<td align="left" width="63%">
Sets the aspect that a rich edit control uses to draw an object. This call does not change the drawing information cached in the object; this must be done by the caller. The call does cause the object to be redrawn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/richole/nf-richole-iricheditole-sethostnames">SetHostNames</a>
</td>
<td align="left" width="63%">
Sets the host names to be given to objects as they are inserted to a rich edit control. The host names are used in the user interface of servers to describe the container context of opened objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/richole/nf-richole-iricheditole-setlinkavailable">SetLinkAvailable</a>
</td>
<td align="left" width="63%">
Sets the value of the link-available bit in the object's flags. The link-available bit defaults to <b>TRUE</b>. It should be set to <b>FALSE</b> if any errors occur on the link which would indicate problems connecting to the linked object or application. When those problems are repaired, the bit should be set to <b>TRUE</b> again.

</td>
</tr>
</table>