---
UID: NE:oaidl.tagFUNCFLAGS
title: FUNCFLAGS (oaidl.h)
description: Specifies function flags.
helpviewer_keywords: ["FUNCFLAGS","FUNCFLAGS enumeration [Automation]","FUNCFLAG_FBINDABLE","FUNCFLAG_FDEFAULTBIND","FUNCFLAG_FDEFAULTCOLLELEM","FUNCFLAG_FDISPLAYBIND","FUNCFLAG_FHIDDEN","FUNCFLAG_FIMMEDIATEBIND","FUNCFLAG_FNONBROWSABLE","FUNCFLAG_FREPLACEABLE","FUNCFLAG_FREQUESTEDIT","FUNCFLAG_FRESTRICTED","FUNCFLAG_FSOURCE","FUNCFLAG_FUIDEFAULT","FUNCFLAG_FUSESGETLASTERROR","_oa96_FUNCFLAGS","automat.funcflags","oaidl/FUNCFLAGS","oaidl/FUNCFLAG_FBINDABLE","oaidl/FUNCFLAG_FDEFAULTBIND","oaidl/FUNCFLAG_FDEFAULTCOLLELEM","oaidl/FUNCFLAG_FDISPLAYBIND","oaidl/FUNCFLAG_FHIDDEN","oaidl/FUNCFLAG_FIMMEDIATEBIND","oaidl/FUNCFLAG_FNONBROWSABLE","oaidl/FUNCFLAG_FREPLACEABLE","oaidl/FUNCFLAG_FREQUESTEDIT","oaidl/FUNCFLAG_FRESTRICTED","oaidl/FUNCFLAG_FSOURCE","oaidl/FUNCFLAG_FUIDEFAULT","oaidl/FUNCFLAG_FUSESGETLASTERROR"]
old-location: automat\funcflags.htm
tech.root: automat
ms.assetid: 290f8769-dde4-47b9-b3bb-680efc95f532
ms.date: 12/05/2018
ms.keywords: FUNCFLAGS, FUNCFLAGS enumeration [Automation], FUNCFLAG_FBINDABLE, FUNCFLAG_FDEFAULTBIND, FUNCFLAG_FDEFAULTCOLLELEM, FUNCFLAG_FDISPLAYBIND, FUNCFLAG_FHIDDEN, FUNCFLAG_FIMMEDIATEBIND, FUNCFLAG_FNONBROWSABLE, FUNCFLAG_FREPLACEABLE, FUNCFLAG_FREQUESTEDIT, FUNCFLAG_FRESTRICTED, FUNCFLAG_FSOURCE, FUNCFLAG_FUIDEFAULT, FUNCFLAG_FUSESGETLASTERROR, _oa96_FUNCFLAGS, automat.funcflags, oaidl/FUNCFLAGS, oaidl/FUNCFLAG_FBINDABLE, oaidl/FUNCFLAG_FDEFAULTBIND, oaidl/FUNCFLAG_FDEFAULTCOLLELEM, oaidl/FUNCFLAG_FDISPLAYBIND, oaidl/FUNCFLAG_FHIDDEN, oaidl/FUNCFLAG_FIMMEDIATEBIND, oaidl/FUNCFLAG_FNONBROWSABLE, oaidl/FUNCFLAG_FREPLACEABLE, oaidl/FUNCFLAG_FREQUESTEDIT, oaidl/FUNCFLAG_FRESTRICTED, oaidl/FUNCFLAG_FSOURCE, oaidl/FUNCFLAG_FUIDEFAULT, oaidl/FUNCFLAG_FUSESGETLASTERROR
req.header: oaidl.h
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
targetos: Windows
req.typenames: FUNCFLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagFUNCFLAGS
 - oaidl/tagFUNCFLAGS
 - FUNCFLAGS
 - oaidl/FUNCFLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OaIdl.h
api_name:
 - FUNCFLAGS
---

# FUNCFLAGS enumeration


## -description

Specifies function flags.

## -enum-fields

### -field FUNCFLAG_FRESTRICTED:0x1

The function should not be accessible from macro languages. This flag is intended for system-level functions or functions that type browsers should not display.

### -field FUNCFLAG_FSOURCE:0x2

The function returns an object that is a source of events.

### -field FUNCFLAG_FBINDABLE:0x4

The function that supports data binding.

### -field FUNCFLAG_FREQUESTEDIT:0x8

When set, any call to a method that sets the property results first in a call to <b>IPropertyNotifySink::OnRequestEdit</b>. The implementation of <b>OnRequestEdit</b> determines if the call is allowed to set the property.

### -field FUNCFLAG_FDISPLAYBIND:0x10

The function that is displayed to the user as bindable. FUNC_FBINDABLE must also be set.

### -field FUNCFLAG_FDEFAULTBIND:0x20

The function that best represents the object. Only one function in a type information can have this attribute.

### -field FUNCFLAG_FHIDDEN:0x40

The function should not be displayed to the user, although it exists and is bindable.

### -field FUNCFLAG_FUSESGETLASTERROR:0x80

The function supports <b>GetLastError</b>. If an error occurs during the function, the caller can call <b>GetLastError</b> to retrieve the error code.

### -field FUNCFLAG_FDEFAULTCOLLELEM:0x100

Permits an optimization in which the compiler looks for a member named xyz on the type of abc. If such a member is found and is flagged as an accessor function for an element of the default collection, then a call is generated to that member function. Permitted on members in dispinterfaces and interfaces; not permitted on modules. For more information, refer to defaultcollelem in Type Libraries and the Object Description Language.

### -field FUNCFLAG_FUIDEFAULT:0x200

The type information member is the default member for display in the user interface.

### -field FUNCFLAG_FNONBROWSABLE:0x400

The property appears in an object browser, but not in a properties browser.

### -field FUNCFLAG_FREPLACEABLE:0x800

Tags the interface as having default behaviors.

### -field FUNCFLAG_FIMMEDIATEBIND:0x1000

Mapped as individual bindable properties.

## -remarks

FUNCFLAG_FHIDDEN means that the property should never be shown in object browsers, property browsers, and so on. This function is useful for removing items from an object model. Code can bind to the member, but the user will never know that the member exists.

FUNCFLAG_FNONBROWSABLE means that the property should not be displayed in a properties browser. It is used in circumstances in which an error would occur if the property were shown in a properties browser.

FUNCFLAG_FRESRICTED means that macro-oriented programmers should not be allowed to access this member. These members are usually treated as _FHIDDEN by tools such as Visual Basic, with the main difference being that code cannot bind to those members.

