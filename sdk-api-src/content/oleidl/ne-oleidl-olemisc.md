---
UID: NE:oleidl.tagOLEMISC
title: OLEMISC (oleidl.h)
description: Describes miscellaneous characteristics of an object or class of objects.
helpviewer_keywords: ["OLEMISC","OLEMISC enumeration [COM]","OLEMISC_ACTIVATEWHENVISIBLE","OLEMISC_ACTSLIKEBUTTON","OLEMISC_ACTSLIKELABEL","OLEMISC_ALIGNABLE","OLEMISC_ALWAYSRUN","OLEMISC_CANLINKBYOLE1","OLEMISC_CANTLINKINSIDE","OLEMISC_IGNOREACTIVATEWHENVISIBLE","OLEMISC_IMEMODE","OLEMISC_INSERTNOTREPLACE","OLEMISC_INSIDEOUT","OLEMISC_INVISIBLEATRUNTIME","OLEMISC_ISLINKOBJECT","OLEMISC_NOUIACTIVATE","OLEMISC_ONLYICONIC","OLEMISC_RECOMPOSEONRESIZE","OLEMISC_RENDERINGISDEVICEINDEPENDENT","OLEMISC_SETCLIENTSITEFIRST","OLEMISC_SIMPLEFRAME","OLEMISC_STATIC","OLEMISC_SUPPORTSMULTILEVELUNDO","OLEMISC_WANTSTOMENUMERGE","_ole_OLEMISC","com.olemisc","oleidl/OLEMISC","oleidl/OLEMISC_ACTIVATEWHENVISIBLE","oleidl/OLEMISC_ACTSLIKEBUTTON","oleidl/OLEMISC_ACTSLIKELABEL","oleidl/OLEMISC_ALIGNABLE","oleidl/OLEMISC_ALWAYSRUN","oleidl/OLEMISC_CANLINKBYOLE1","oleidl/OLEMISC_CANTLINKINSIDE","oleidl/OLEMISC_IGNOREACTIVATEWHENVISIBLE","oleidl/OLEMISC_IMEMODE","oleidl/OLEMISC_INSERTNOTREPLACE","oleidl/OLEMISC_INSIDEOUT","oleidl/OLEMISC_INVISIBLEATRUNTIME","oleidl/OLEMISC_ISLINKOBJECT","oleidl/OLEMISC_NOUIACTIVATE","oleidl/OLEMISC_ONLYICONIC","oleidl/OLEMISC_RECOMPOSEONRESIZE","oleidl/OLEMISC_RENDERINGISDEVICEINDEPENDENT","oleidl/OLEMISC_SETCLIENTSITEFIRST","oleidl/OLEMISC_SIMPLEFRAME","oleidl/OLEMISC_STATIC","oleidl/OLEMISC_SUPPORTSMULTILEVELUNDO","oleidl/OLEMISC_WANTSTOMENUMERGE"]
old-location: com\olemisc.htm
tech.root: com
ms.assetid: 0a90d126-fc28-460c-8eaf-cf98ae998f95
ms.date: 12/05/2018
ms.keywords: OLEMISC, OLEMISC enumeration [COM], OLEMISC_ACTIVATEWHENVISIBLE, OLEMISC_ACTSLIKEBUTTON, OLEMISC_ACTSLIKELABEL, OLEMISC_ALIGNABLE, OLEMISC_ALWAYSRUN, OLEMISC_CANLINKBYOLE1, OLEMISC_CANTLINKINSIDE, OLEMISC_IGNOREACTIVATEWHENVISIBLE, OLEMISC_IMEMODE, OLEMISC_INSERTNOTREPLACE, OLEMISC_INSIDEOUT, OLEMISC_INVISIBLEATRUNTIME, OLEMISC_ISLINKOBJECT, OLEMISC_NOUIACTIVATE, OLEMISC_ONLYICONIC, OLEMISC_RECOMPOSEONRESIZE, OLEMISC_RENDERINGISDEVICEINDEPENDENT, OLEMISC_SETCLIENTSITEFIRST, OLEMISC_SIMPLEFRAME, OLEMISC_STATIC, OLEMISC_SUPPORTSMULTILEVELUNDO, OLEMISC_WANTSTOMENUMERGE, _ole_OLEMISC, com.olemisc, oleidl/OLEMISC, oleidl/OLEMISC_ACTIVATEWHENVISIBLE, oleidl/OLEMISC_ACTSLIKEBUTTON, oleidl/OLEMISC_ACTSLIKELABEL, oleidl/OLEMISC_ALIGNABLE, oleidl/OLEMISC_ALWAYSRUN, oleidl/OLEMISC_CANLINKBYOLE1, oleidl/OLEMISC_CANTLINKINSIDE, oleidl/OLEMISC_IGNOREACTIVATEWHENVISIBLE, oleidl/OLEMISC_IMEMODE, oleidl/OLEMISC_INSERTNOTREPLACE, oleidl/OLEMISC_INSIDEOUT, oleidl/OLEMISC_INVISIBLEATRUNTIME, oleidl/OLEMISC_ISLINKOBJECT, oleidl/OLEMISC_NOUIACTIVATE, oleidl/OLEMISC_ONLYICONIC, oleidl/OLEMISC_RECOMPOSEONRESIZE, oleidl/OLEMISC_RENDERINGISDEVICEINDEPENDENT, oleidl/OLEMISC_SETCLIENTSITEFIRST, oleidl/OLEMISC_SIMPLEFRAME, oleidl/OLEMISC_STATIC, oleidl/OLEMISC_SUPPORTSMULTILEVELUNDO, oleidl/OLEMISC_WANTSTOMENUMERGE
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: OLEMISC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOLEMISC
 - oleidl/tagOLEMISC
 - OLEMISC
 - oleidl/OLEMISC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OleIdl.h
api_name:
 - OLEMISC
---

# OLEMISC enumeration


## -description

Describes miscellaneous characteristics of an object or class of objects. A container can call the <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getmiscstatus">IOleObject::GetMiscStatus</a> method to determine the <b>OLEMISC</b> bits set for an object. The values specified in an object server's CLSID\MiscStatus entry in the registration database are based on the <b>OLEMISC</b> enumeration. These constants are also used in the <b>dwStatus</b> member of the <a href="/windows/desktop/api/oleidl/ns-oleidl-objectdescriptor">OBJECTDESCRIPTOR</a> structure.

## -enum-fields

### -field OLEMISC_RECOMPOSEONRESIZE:0x1

When the container resizes the space allocated to displaying one of the object's presentations, the object wants to recompose the presentation. This means that on resize, the object wants to do more than scale its picture. If this bit is set, the container should force the object to the running state and call <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setextent">IOleObject::SetExtent</a> with the new size.

### -field OLEMISC_ONLYICONIC:0x2

The object has no useful content view other than its icon. From the user's perspective, the <b>Display As Icon</b> check box (in the <b>Paste Special</b> dialog box) for this object should always be checked, and should not be uncheckable. Note that such an object should still have a drawable content aspect; it will look the same as its icon view.

### -field OLEMISC_INSERTNOTREPLACE:0x4

The object has initialized itself from the data in the container's current selection. Containers should examine this bit after calling <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-initfromdata">IOleObject::InitFromData</a> to initialize an object from the current selection. If set, the container should insert the object beside the current selection rather than replacing the current selection. If this bit is not set, the object being inserted replaces the current selection.

### -field OLEMISC_STATIC:0x8

This object is a static object, which is an object that contains only a presentation; it contains no native data. See <a href="/windows/desktop/api/ole2/nf-ole2-olecreatestaticfromdata">OleCreateStaticFromData</a>.

### -field OLEMISC_CANTLINKINSIDE:0x10

This object cannot be the link source that when bound to activates (runs) the object. If the object is selected and copied to the clipboard, the object's container can offer a link in a clipboard data transfer that, when bound, must connect to the outside of the object. The user would see the object selected in its container, not open for editing. Rather than doing this, the container can simply refuse to offer a link source when transferring objects with this bit set. Examples of objects that have this bit set include OLE1 objects, static objects, and links.

### -field OLEMISC_CANLINKBYOLE1:0x20

This object can be linked to by OLE 1 containers. This bit is used in the <b>dwStatus</b> member of the <a href="/windows/desktop/api/oleidl/ns-oleidl-objectdescriptor">OBJECTDESCRIPTOR</a> structure transferred with the Object and Link Source Descriptor formats. An object can be linked to by OLE 1 containers if it is an untitled document, a file, or a selection of data within a file. Embedded objects or pseudo-objects that are contained within an embedded object cannot be linked to by OLE 1 containers (i.e., OLE 1 containers cannot link to link sources that, when bound, require more than one object server to be run.

### -field OLEMISC_ISLINKOBJECT:0x40

This object is a link object. This bit is significant to OLE 1 and is set by the OLE 2 link object; object applications have no need to set this bit.

### -field OLEMISC_INSIDEOUT:0x80

This object is capable of activating in-place, without requiring installation of menus and toolbars to run. Several such objects can be active concurrently. Some containers, such as forms, may choose to activate such objects automatically.

### -field OLEMISC_ACTIVATEWHENVISIBLE:0x100

This bit is set only when OLEMISC_INSIDEOUT is set, and indicates that this object prefers to be activated whenever it is visible. Some containers may always ignore this hint.

### -field OLEMISC_RENDERINGISDEVICEINDEPENDENT:0x200

This object does not pay any attention to target devices. Its presentation data will be the same in all cases.

### -field OLEMISC_INVISIBLEATRUNTIME:0x400

This value is used with controls. It indicates that the control has no run-time user interface, but that it should be visible at design time. For example, a timer control that fires a specific event periodically would not show itself at run time, but it needs a design-time user interface so a form designer can set the event period and other properties.

### -field OLEMISC_ALWAYSRUN:0x800

This value is used with controls. It tells the container that this control always wants to be running. As a result, the container should call <a href="/windows/desktop/api/ole2/nf-ole2-olerun">OleRun</a> when loading or creating the object.

### -field OLEMISC_ACTSLIKEBUTTON:0x1000

This value is used with controls. It indicates that the control is buttonlike in that it understands and obeys the container's DisplayAsDefault ambient property.

### -field OLEMISC_ACTSLIKELABEL:0x2000

This value is used with controls. It marks the control as a label for whatever control comes after it in the form's ordering. Pressing a mnemonic key for a label control activates the control after it.

### -field OLEMISC_NOUIACTIVATE:0x4000

This value is used with controls. It indicates that the control has no UI active state, meaning that it requires no in-place tools, no shared menu, and no accelerators. It also means that the control never needs the focus.

### -field OLEMISC_ALIGNABLE:0x8000

This value is used with controls. It indicates that the control understands how to align itself within its display rectangle, according to alignment properties such as left, center, and right.

### -field OLEMISC_SIMPLEFRAME:0x10000

This value is used with controls. It indicates that the control is a simple grouping of other controls and does little more than pass Windows messages to the control container managing the form. Controls of this sort require the implementation of <a href="/windows/desktop/api/ocidl/nn-ocidl-isimpleframesite">ISimpleFrameSite</a> on the container's site.

### -field OLEMISC_SETCLIENTSITEFIRST:0x20000

This value is used with controls. It indicates that the control wants to use <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setclientsite">IOleObject::SetClientSite</a> as its initialization function, even before a call such as <a href="/windows/desktop/api/ocidl/nf-ocidl-ipersiststreaminit-initnew">IPersistStreamInit::InitNew</a> or <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-initnew">IPersistStorage::InitNew</a>. This allows the control to access a container's ambient properties before loading information from persistent storage. Note that the current implementations of <a href="/windows/desktop/api/ole/nf-ole-olecreate">OleCreate</a>, <a href="/windows/desktop/api/ole2/nf-ole2-olecreatefromdata">OleCreateFromData</a>, <a href="/windows/desktop/api/ole/nf-ole-olecreatefromfile">OleCreateFromFile</a>, <a href="/windows/desktop/api/ole2/nf-ole2-oleload">OleLoad</a>, and the default handler do not understand this value. Control containers that wish to honor this value must currently implement their own versions of these functions in order to establish the correct initialization sequence for the control.

### -field OLEMISC_IMEMODE:0x40000

Obsolete. A control that works with an Input Method Editor (IME) system component can control the state of the IME through the IMEMode property rather than using this value in the <a href="/windows/desktop/api/oleidl/ne-oleidl-olemisc">OLEMISC</a> enumeration. You can use an IME component to enter information in Asian character sets with a regular keyboard. A Japanese IME, for example, allows you to type a word such as "sushi," on a regular keyboard and when you hit the spacebar, the IME component converts that word to appropriate kanji or proposes possible choices. The OLEMISC_IMEMODE value was previously used to mark a control as capable of controlling an IME mode system component.

### -field OLEMISC_IGNOREACTIVATEWHENVISIBLE:0x80000

For new ActiveX controls to work in an older container, the control may need to have the OLEMISC_ACTIVATEWHENVISIBLE value set. However, in a newer container that understands and uses IPointerInactive, the control does not wish to be in-place activated when it becomes visible. To allow the control to work in both kinds of containers, the control can set this value. Then, the container ignores OLEMISC_ACTIVATEWHENVISIBLE and does not in-place activate the control when it becomes visible.

### -field OLEMISC_WANTSTOMENUMERGE:0x100000

A control that can merge its menu with its container sets this value.

### -field OLEMISC_SUPPORTSMULTILEVELUNDO:0x200000

A control that supports multi-level undo sets this value.

## -see-also

<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getmiscstatus">IOleObject::GetMiscStatus</a>



<a href="/windows/desktop/api/oleidl/ns-oleidl-objectdescriptor">OBJECTDESCRIPTOR</a>
