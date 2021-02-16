---
UID: NF:oleidl.IOleObject.DoVerb
title: IOleObject::DoVerb (oleidl.h)
description: Requests that an object perform an action in response to an end-user's action. The possible actions are enumerated for the object in IOleObject::EnumVerbs.
helpviewer_keywords: ["DoVerb","DoVerb method [COM]","DoVerb method [COM]","IOleObject interface","IOleObject interface [COM]","DoVerb method","IOleObject.DoVerb","IOleObject::DoVerb","_ole_ioleobject_doverb","com.ioleobject_doverb","oleidl/IOleObject::DoVerb"]
old-location: com\ioleobject_doverb.htm
tech.root: com
ms.assetid: fabd6a0a-7b0c-4c99-af22-8b117addd5f7
ms.date: 12/05/2018
ms.keywords: DoVerb, DoVerb method [COM], DoVerb method [COM],IOleObject interface, IOleObject interface [COM],DoVerb method, IOleObject.DoVerb, IOleObject::DoVerb, _ole_ioleobject_doverb, com.ioleobject_doverb, oleidl/IOleObject::DoVerb
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOleObject::DoVerb
 - oleidl/IOleObject::DoVerb
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleObject.DoVerb
---

# IOleObject::DoVerb


## -description

Requests that an object perform an action in response to an end-user's action. The possible actions are enumerated for the object in <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-enumverbs">IOleObject::EnumVerbs</a>.

## -parameters

### -param iVerb [in]

Number assigned to the verb in the <a href="/windows/desktop/api/oleidl/ns-oleidl-oleverb">OLEVERB</a> structure returned by <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-enumverbs">IOleObject::EnumVerbs</a>.

### -param lpmsg [in]

Pointer to the <a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a> structure describing the event (such as a double-click) that invoked the verb. The caller should pass the <b>MSG</b> structure unmodified, without attempting to interpret or alter the values of any of the structure members.

### -param pActiveSite [in]

Pointer to the <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleclientsite">IOleClientSite</a> interface on the object's active client site, where the event occurred that invoked the verb.

### -param lindex [in]

This parameter is reserved and must be zero.

### -param hwndParent [in]

Handle of the document window containing the object. This and <i>lprcPosRect</i> together make it possible to open a temporary window for an object, where <i>hwndParent</i> is the parent window in which the object's window is to be displayed, and <i>lprcPosRect</i> defines the area available for displaying the object window within that parent. A temporary window is useful, for example, to a multimedia object that opens itself for playback but not for editing.

### -param lprcPosRect [in]

Pointer to the <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure containing the coordinates, in pixels, that define an object's bounding rectangle in <i>hwndParent</i>. This and <i>hwndParent</i> together enable opening multimedia objects for playback but not for editing.

## -returns

This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_NOT_INPLACEACTIVE</b></dt>
</dl>
</td>
<td width="60%">
iVerb set to OLEIVERB_UIACTIVATE or OLEIVERB_INPLACEACTIVATE and object is not already visible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_CANT_BINDTOSOURCE</b></dt>
</dl>
</td>
<td width="60%">
The object handler or link object cannot connect to the link source.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_LINDEX</b></dt>
</dl>
</td>
<td width="60%">
Invalid lindex.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEOBJ_S_CANNOT_DOVERB_NOW</b></dt>
</dl>
</td>
<td width="60%">
The verb is valid, but in the object's current state it cannot carry out the corresponding action.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEOBJ_S_INVALIDHWND</b></dt>
</dl>
</td>
<td width="60%">
DoVerb was successful but <i>hwndParent</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEOBJ_E_NOVERBS</b></dt>
</dl>
</td>
<td width="60%">
The object does not support any verbs.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEOBJ_S_INVALIDVERB</b></dt>
</dl>
</td>
<td width="60%">
Link source is across a network that is not connected to a drive on this computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_CONNECT</b></dt>
</dl>
</td>
<td width="60%">
Link source is across a network that is not connected to a drive on this computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_CLASSDIFF</b></dt>
</dl>
</td>
<td width="60%">
Class for source of link has undergone a conversion.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Object does not support in-place activation or does not recognize a negative verb number.

</td>
</tr>
</table>

## -remarks

A "verb" is an action that an OLE object takes in response to a message from its container. An object's container, or a client linked to the object, normally calls <b>IOleObject::DoVerb</b> in response to some end-user action, such as double-clicking on the object. The various actions that are available for a given object are enumerated in an <a href="/windows/desktop/api/oleidl/ns-oleidl-oleverb">OLEVERB</a> structure, which the container obtains by calling <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-enumverbs">IOleObject::EnumVerbs</a>. <b>IOleObject::DoVerb</b> matches the value of iVerb against the iVerb member of the structure to determine which verb to invoke.

Through <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-enumverbs">IOleObject::EnumVerbs</a>, an object, rather than its container, determines which verbs (i.e., actions) it supports. OLE 2 defines seven verbs that are available, but not necessarily useful, to all objects. In addition, each object can define additional verbs that are unique to it. The following table describes the verbs defined by OLE.

<table>
<tr>
<th>Verb</th>
<th>Description</th>
</tr>
<tr>
<td>
OLEIVERB_PRIMARY (0L)

</td>
<td>
Specifies the action that occurs when an end user double-clicks the object in its container. The object, not the container, determines this action. If the object supports in-place activation, the primary verb usually activates the object in place.

</td>
</tr>
<tr>
<td>
OLEIVERB_SHOW (-1)

</td>
<td>
Instructs an object to show itself for editing or viewing. Called to display newly inserted objects for initial editing and to show link sources. Usually an alias for some other object-defined verb.

</td>
</tr>
<tr>
<td>
OLEIVERB_OPEN (-2)

</td>
<td>
Instructs an object, including one that otherwise supports in-place activation, to open itself for editing in a window separate from that of its container. If the object does not support in-place activation, this verb has the same semantics as OLEIVERB_SHOW.

</td>
</tr>
<tr>
<td>
OLEIVERB_HIDE (-3)

</td>
<td>
Causes an object to remove its user interface from the view. Applies only to objects that are activated in-place.

</td>
</tr>
<tr>
<td>
OLEIVERB_UIACTIVATE (-4)

</td>
<td>
Activates an object in place, along with its full set of user-interface tools, including menus, toolbars, and its name in the title bar of the container window. If the object does not support in-place activation, it should return E_NOTIMPL.

</td>
</tr>
<tr>
<td>
OLEIVERB_INPLACEACTIVATE (-5)

</td>
<td>
Activates an object in place without displaying tools, such as menus and toolbars, that end users need to change the behavior or appearance of the object. Single-clicking such an object causes it to negotiate the display of its user-interface tools with its container. If the container refuses, the object remains active but without its tools displayed.

</td>
</tr>
<tr>
<td>
OLEIVERB_DISCARDUNDOSTATE (-6)

</td>
<td>
Used to tell objects to discard any undo state that they may be maintaining without deactivating the object.

</td>
</tr>
</table>
 

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Containers call <b>IOleObject::DoVerb</b> as part of initializing a newly created object. Before making the call, containers should first call <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setclientsite">IOleObject::SetClientSite</a> to inform the object of its display location and <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-sethostnames">IOleObject::SetHostNames</a> to alert the object that it is an embedded object and to trigger appropriate changes to the user interface of the object application in preparation for opening an editing window.

<b>IOleObject::DoVerb</b> automatically runs the OLE server application. If an error occurs during verb execution, the object application is shut down.

If an end user invokes a verb by some means other than selecting a command from a menu (say, by double-clicking or, more rarely, single-clicking an object), the object's container should pass a pointer to a Windows <a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a> structure containing the appropriate message. For example, if the end user invokes a verb by double-clicking the object, the container should pass a <b>MSG</b> structure containing WM_LBUTTONDBLCLK, WM_MBUTTONDBLCLK, or WM_RBUTTONDBLCLK. If the container passes no message, lpmsg should be set to <b>NULL</b>. The object should ignore the <b>hwnd</b> member of the passed <b>MSG</b> structure, but can use all the other MSG members.

If the object's embedding container calls <b>IOleObject::DoVerb</b>, the client-site pointer (<i>pClientSite</i>) passed to <b>IOleObject::DoVerb</b> is the same as that of the embedding site. If the embedded object is a link source, the pointer passed to <b>IOleObject::DoVerb</b> is that of the linking client's client site.

When <b>IOleObject::DoVerb</b> is invoked on an OLE link, it may return OLE_E_CLASSDIFF or MK_CONNECTMANUALLY. The link object returns the former error when the link source has been subjected to some sort of conversion while the link was passive. The link object returns the latter error when the link source is located on a network drive that is not currently connected to the caller's computer. The only way to connect a link under these conditions is to first call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a>, ask for <a href="/windows/desktop/api/oleidl/nn-oleidl-iolelink">IOleLink</a>, allocate a bind context, and run the link source by calling <a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-bindtosource">IOleLink::BindToSource</a>.

Container applications that do not support general in-place activation can still use the <i>hwndParent</i> and <i>lprcPosRect</i> parameters to support in-place playback of multimedia files. Containers must pass valid <i>hwndParent</i> and <i>lprcPosRect</i> parameters to <b>IOleObject::DoVerb</b>.

Some code samples pass a lindex value of -1 instead of zero. The value -1 works but should be avoided in favor of zero. The <i>lindex</i> parameter is a reserved parameter, and for reasons of consistency Microsoft recommends assigning a zero value to all reserved parameters.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
In addition to the above verbs, an object can define in its <a href="/windows/desktop/api/oleidl/ns-oleidl-oleverb">OLEVERB</a> structure additional verbs that are specific to itself. Positive numbers designate these object-specific verbs. An object should treat any unknown positive verb number as if it were the primary verb and return OLEOBJ_S_INVALIDVERB to the calling function. The object should ignore verbs with negative numbers that it does not recognize and return E_NOTIMPL.

If the verb being executed places the object in the running state, you should register the object in the running object table (ROT) even if its server application doesn't support linking. Registration is important because the object at some point may serve as the source of a link in a container that supports links to embeddings. Registering the object with the ROT enables the link client to get a pointer to the object directly, instead of having to go through the object's container. To perform the registration, call <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleclientsite-getmoniker">IOleClientSite::GetMoniker</a> to get the full moniker of the object, call the <a href="/windows/desktop/api/objbase/nf-objbase-getrunningobjecttable">GetRunningObjectTable</a> function to get a pointer to the ROT, and then call <a href="/windows/desktop/api/objidl/nf-objidl-irunningobjecttable-register">IRunningObjectTable::Register</a>.

<div class="alert"><b>Note</b>  When the object leaves the running state, remember to revoke the object's registration with the ROT by calling <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-close">IOleObject::Close</a>. If the object's container document is renamed while the object is running, you should revoke the object's registration and re-register it with the ROT, using its new name. The container should inform the object of its new moniker either by calling <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setmoniker">IOleObject::SetMoniker</a> or by responding to the object's calling <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleclientsite-getmoniker">IOleClientSite::GetMoniker</a>.</div>
<div> </div>
When showing a window as a result of <b>IOleObject::DoVerb</b>, it is very important for the object to explicitly call <a href="/windows/desktop/api/winuser/nf-winuser-setforegroundwindow">SetForegroundWindow</a> on its editing window. This ensures that the object's window will be visible to the user even if another process originally obscured it. For more information see <b>SetForegroundWindow</b> and <a href="/windows/desktop/api/winuser/nf-winuser-setactivewindow">SetActiveWindow</a>.

## -see-also

<a href="/windows/desktop/api/objbase/nf-objbase-getrunningobjecttable">GetRunningObjectTable</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleclientsite-getmoniker">IOleClientSite::GetMoniker</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-bindtosource">IOleLink::BindToSource</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-close">IOleObject::Close</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-enumverbs">IOleObject::EnumVerbs</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getmoniker">IOleObject::GetMoniker</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setmoniker">IOleObject::SetMoniker</a>



<a href="/windows/desktop/api/objidl/nf-objidl-irunningobjecttable-register">IRunningObjectTable::Register</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olerun">OleRun</a>