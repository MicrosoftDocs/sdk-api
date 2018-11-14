---
UID: NE:oleidl.tagOLEMISC
title: tagOLEMISC
author: windows-sdk-content
description: Describes miscellaneous characteristics of an object or class of objects.
old-location: com\olemisc.htm
tech.root: com
ms.assetid: 0a90d126-fc28-460c-8eaf-cf98ae998f95
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: OLEMISC, OLEMISC enumeration [COM], OLEMISC_ACTIVATEWHENVISIBLE, OLEMISC_ACTSLIKEBUTTON, OLEMISC_ACTSLIKELABEL, OLEMISC_ALIGNABLE, OLEMISC_ALWAYSRUN, OLEMISC_CANLINKBYOLE1, OLEMISC_CANTLINKINSIDE, OLEMISC_IGNOREACTIVATEWHENVISIBLE, OLEMISC_IMEMODE, OLEMISC_INSERTNOTREPLACE, OLEMISC_INSIDEOUT, OLEMISC_INVISIBLEATRUNTIME, OLEMISC_ISLINKOBJECT, OLEMISC_NOUIACTIVATE, OLEMISC_ONLYICONIC, OLEMISC_RECOMPOSEONRESIZE, OLEMISC_RENDERINGISDEVICEINDEPENDENT, OLEMISC_SETCLIENTSITEFIRST, OLEMISC_SIMPLEFRAME, OLEMISC_STATIC, OLEMISC_SUPPORTSMULTILEVELUNDO, OLEMISC_WANTSTOMENUMERGE, _ole_OLEMISC, com.olemisc, oleidl/OLEMISC, oleidl/OLEMISC_ACTIVATEWHENVISIBLE, oleidl/OLEMISC_ACTSLIKEBUTTON, oleidl/OLEMISC_ACTSLIKELABEL, oleidl/OLEMISC_ALIGNABLE, oleidl/OLEMISC_ALWAYSRUN, oleidl/OLEMISC_CANLINKBYOLE1, oleidl/OLEMISC_CANTLINKINSIDE, oleidl/OLEMISC_IGNOREACTIVATEWHENVISIBLE, oleidl/OLEMISC_IMEMODE, oleidl/OLEMISC_INSERTNOTREPLACE, oleidl/OLEMISC_INSIDEOUT, oleidl/OLEMISC_INVISIBLEATRUNTIME, oleidl/OLEMISC_ISLINKOBJECT, oleidl/OLEMISC_NOUIACTIVATE, oleidl/OLEMISC_ONLYICONIC, oleidl/OLEMISC_RECOMPOSEONRESIZE, oleidl/OLEMISC_RENDERINGISDEVICEINDEPENDENT, oleidl/OLEMISC_SETCLIENTSITEFIRST, oleidl/OLEMISC_SIMPLEFRAME, oleidl/OLEMISC_STATIC, oleidl/OLEMISC_SUPPORTSMULTILEVELUNDO, oleidl/OLEMISC_WANTSTOMENUMERGE, tagOLEMISC
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OleIdl.h
api_name:
 - OLEMISC
product: Windows
targetos: Windows
req.typenames: OLEMISC
req.redist: 
---

# tagOLEMISC enumeration


## -description


Describes miscellaneous characteristics of an object or class of objects. A container can call the <a href="https://msdn.microsoft.com/0c5e9f73-8eec-48e0-a172-4d3d49e56071">IOleObject::GetMiscStatus</a> method to determine the <b>OLEMISC</b> bits set for an object. The values specified in an object server's CLSID\MiscStatus entry in the registration database are based on the <b>OLEMISC</b> enumeration. These constants are also used in the <b>dwStatus</b> member of the <a href="https://msdn.microsoft.com/5865e16b-c1a5-4bfd-8d94-c2f8f73b1205">OBJECTDESCRIPTOR</a> structure.


## -enum-fields




### -field OLEMISC_RECOMPOSEONRESIZE

When the container resizes the space allocated to displaying one of the object's presentations, the object wants to recompose the presentation. This means that on resize, the object wants to do more than scale its picture. If this bit is set, the container should force the object to the running state and call <a href="https://msdn.microsoft.com/f1960095-7c9a-4058-aef1-f31e3d6e3509">IOleObject::SetExtent</a> with the new size.


### -field OLEMISC_ONLYICONIC

The object has no useful content view other than its icon. From the user's perspective, the <b>Display As Icon</b> check box (in the <b>Paste Special</b> dialog box) for this object should always be checked, and should not be uncheckable. Note that such an object should still have a drawable content aspect; it will look the same as its icon view.


### -field OLEMISC_INSERTNOTREPLACE

The object has initialized itself from the data in the container's current selection. Containers should examine this bit after calling <a href="https://msdn.microsoft.com/8bbda602-4421-4f79-a33a-63ded9a8bf90">IOleObject::InitFromData</a> to initialize an object from the current selection. If set, the container should insert the object beside the current selection rather than replacing the current selection. If this bit is not set, the object being inserted replaces the current selection.


### -field OLEMISC_STATIC

This object is a static object, which is an object that contains only a presentation; it contains no native data. See <a href="https://msdn.microsoft.com/847d82f5-149d-48a4-a228-f5551a07a790">OleCreateStaticFromData</a>.


### -field OLEMISC_CANTLINKINSIDE

This object cannot be the link source that when bound to activates (runs) the object. If the object is selected and copied to the clipboard, the object's container can offer a link in a clipboard data transfer that, when bound, must connect to the outside of the object. The user would see the object selected in its container, not open for editing. Rather than doing this, the container can simply refuse to offer a link source when transferring objects with this bit set. Examples of objects that have this bit set include OLE1 objects, static objects, and links.


### -field OLEMISC_CANLINKBYOLE1

This object can be linked to by OLE 1 containers. This bit is used in the <b>dwStatus</b> member of the <a href="https://msdn.microsoft.com/5865e16b-c1a5-4bfd-8d94-c2f8f73b1205">OBJECTDESCRIPTOR</a> structure transferred with the Object and Link Source Descriptor formats. An object can be linked to by OLE 1 containers if it is an untitled document, a file, or a selection of data within a file. Embedded objects or pseudo-objects that are contained within an embedded object cannot be linked to by OLE 1 containers (i.e., OLE 1 containers cannot link to link sources that, when bound, require more than one object server to be run.


### -field OLEMISC_ISLINKOBJECT

This object is a link object. This bit is significant to OLE 1 and is set by the OLE 2 link object; object applications have no need to set this bit.


### -field OLEMISC_INSIDEOUT

This object is capable of activating in-place, without requiring installation of menus and toolbars to run. Several such objects can be active concurrently. Some containers, such as forms, may choose to activate such objects automatically.


### -field OLEMISC_ACTIVATEWHENVISIBLE

This bit is set only when OLEMISC_INSIDEOUT is set, and indicates that this object prefers to be activated whenever it is visible. Some containers may always ignore this hint.


### -field OLEMISC_RENDERINGISDEVICEINDEPENDENT

This object does not pay any attention to target devices. Its presention data will be the same in all cases.


### -field OLEMISC_INVISIBLEATRUNTIME

This value is used with controls. It indicates that the control has no run-time user interface, but that it should be visible at design time. For example, a timer control that fires a specific event periodically would not show itself at run time, but it needs a design-time user interface so a form designer can set the event period and other properties.


### -field OLEMISC_ALWAYSRUN

This value is used with controls. It tells the container that this control always wants to be running. As a result, the container should call <a href="https://msdn.microsoft.com/9035f996-b163-4855-aa9d-184b77072ead">OleRun</a> when loading or creating the object.


### -field OLEMISC_ACTSLIKEBUTTON

This value is used with controls. It indicates that the control is buttonlike in that it understands and obeys the container's DisplayAsDefault ambient property.


### -field OLEMISC_ACTSLIKELABEL

This value is used with controls. It marks the control as a label for whatever control comes after it in the form's ordering. Pressing a mnemonic key for a label control activates the control after it.


### -field OLEMISC_NOUIACTIVATE

This value is used with controls. It indicates that the control has no UI active state, meaning that it requires no in-place tools, no shared menu, and no accelerators. It also means that the control never needs the focus.


### -field OLEMISC_ALIGNABLE

This value is used with controls. It indicates that the control understands how to align itself within its display rectangle, according to alignment properties such as left, center, and right.


### -field OLEMISC_SIMPLEFRAME

This value is used with controls. It indicates that the control is a simple grouping of other controls and does little more than pass Windows messages to the control container managing the form. Controls of this sort require the implementation of <a href="https://msdn.microsoft.com/ccddeae4-14fc-47df-a612-83d48a479b48">ISimpleFrameSite</a> on the container's site.


### -field OLEMISC_SETCLIENTSITEFIRST

This value is used with controls. It indicates that the control wants to use <a href="https://msdn.microsoft.com/6690b5a3-bada-496c-89cb-a9ae1fc9dfb0">IOleObject::SetClientSite</a> as its initialization function, even before a call such as <a href="https://msdn.microsoft.com/9e318698-0c3c-41c2-bb9e-04e8c9746c4d">IPersistStreamInit::InitNew</a> or <a href="https://msdn.microsoft.com/79caf1f6-d974-4aee-8563-eda4876a0a90">IPersistStorage::InitNew</a>. This allows the control to access a container's ambient properties before loading information from persistent storage. Note that the current implementations of <a href="https://msdn.microsoft.com/00b7edd2-8e2e-4e0a-91a6-d966f6c8d456">OleCreate</a>, <a href="https://msdn.microsoft.com/aa5e997e-60d4-472d-9c81-5359c277bde3">OleCreateFromData</a>, <a href="https://msdn.microsoft.com/98c63646-6617-46b6-8c3e-82d1c4d0adb6">OleCreateFromFile</a>, <a href="https://msdn.microsoft.com/f2d8bb2e-5bd1-4991-a80c-ed06bfd5c9f9">OleLoad</a>, and the default handler do not understand this value. Control containers that wish to honor this value must currently implement their own versions of these functions in order to establish the correct initialization sequence for the control.


### -field OLEMISC_IMEMODE

Obsolete. A control that works with an Input Method Editor (IME) system component can control the state of the IME through the IMEMode property rather than using this value in the <a href="https://msdn.microsoft.com/0a90d126-fc28-460c-8eaf-cf98ae998f95">OLEMISC</a> enumeration. You can use an IME component to enter information in Asian character sets with a regular keyboard. A Japanese IME, for example, allows you to type a word such as "sushi," on a regular keyboard and when you hit the spacebar, the IME component converts that word to appropriate kanji or proposes possible choices. The OLEMISC_IMEMODE value was previously used to mark a control as capable of controlling an IME mode system component.


### -field OLEMISC_IGNOREACTIVATEWHENVISIBLE

For new ActiveX controls to work in an older container, the control may need to have the OLEMISC_ACTIVATEWHENVISIBLE value set. However, in a newer container that understands and uses IPointerInactive, the control does not wish to be in-place activated when it becomes visible. To allow the control to work in both kinds of containers, the control can set this value. Then, the container ignores OLEMISC_ACTIVATEWHENVISIBLE and does not in-place activate the control when it becomes visible.


### -field OLEMISC_WANTSTOMENUMERGE

A control that can merge its menu with its container sets this value.


### -field OLEMISC_SUPPORTSMULTILEVELUNDO

A control that supports multi-level undo sets this value.



## -see-also




<a href="https://msdn.microsoft.com/0c5e9f73-8eec-48e0-a172-4d3d49e56071">IOleObject::GetMiscStatus</a>



<a href="https://msdn.microsoft.com/5865e16b-c1a5-4bfd-8d94-c2f8f73b1205">OBJECTDESCRIPTOR</a>
 

 

