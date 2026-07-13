---
UID: NE:oaidl.tagVARFLAGS
title: VARFLAGS (oaidl.h)
description: Specifies variable flags.
helpviewer_keywords: ["VARFLAGS","VARFLAGS enumeration [Automation]","VARFLAG_FBINDABLE","VARFLAG_FDEFAULTBIND","VARFLAG_FDEFAULTCOLLELEM","VARFLAG_FDISPLAYBIND","VARFLAG_FHIDDEN","VARFLAG_FIMMEDIATEBIND","VARFLAG_FNONBROWSABLE","VARFLAG_FREADONLY","VARFLAG_FREPLACEABLE","VARFLAG_FREQUESTEDIT","VARFLAG_FRESTRICTED","VARFLAG_FSOURCE","VARFLAG_FUIDEFAULT","_oa96_VARFLAGS","automat.varflags","oaidl/VARFLAGS","oaidl/VARFLAG_FBINDABLE","oaidl/VARFLAG_FDEFAULTBIND","oaidl/VARFLAG_FDEFAULTCOLLELEM","oaidl/VARFLAG_FDISPLAYBIND","oaidl/VARFLAG_FHIDDEN","oaidl/VARFLAG_FIMMEDIATEBIND","oaidl/VARFLAG_FNONBROWSABLE","oaidl/VARFLAG_FREADONLY","oaidl/VARFLAG_FREPLACEABLE","oaidl/VARFLAG_FREQUESTEDIT","oaidl/VARFLAG_FRESTRICTED","oaidl/VARFLAG_FSOURCE","oaidl/VARFLAG_FUIDEFAULT"]
old-location: automat\varflags.htm
tech.root: automat
ms.assetid: 9422f2a5-d8c0-4d65-ad7a-9eaa9bbedf91
ms.date: 12/05/2018
ms.keywords: VARFLAGS, VARFLAGS enumeration [Automation], VARFLAG_FBINDABLE, VARFLAG_FDEFAULTBIND, VARFLAG_FDEFAULTCOLLELEM, VARFLAG_FDISPLAYBIND, VARFLAG_FHIDDEN, VARFLAG_FIMMEDIATEBIND, VARFLAG_FNONBROWSABLE, VARFLAG_FREADONLY, VARFLAG_FREPLACEABLE, VARFLAG_FREQUESTEDIT, VARFLAG_FRESTRICTED, VARFLAG_FSOURCE, VARFLAG_FUIDEFAULT, _oa96_VARFLAGS, automat.varflags, oaidl/VARFLAGS, oaidl/VARFLAG_FBINDABLE, oaidl/VARFLAG_FDEFAULTBIND, oaidl/VARFLAG_FDEFAULTCOLLELEM, oaidl/VARFLAG_FDISPLAYBIND, oaidl/VARFLAG_FHIDDEN, oaidl/VARFLAG_FIMMEDIATEBIND, oaidl/VARFLAG_FNONBROWSABLE, oaidl/VARFLAG_FREADONLY, oaidl/VARFLAG_FREPLACEABLE, oaidl/VARFLAG_FREQUESTEDIT, oaidl/VARFLAG_FRESTRICTED, oaidl/VARFLAG_FSOURCE, oaidl/VARFLAG_FUIDEFAULT
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
req.typenames: VARFLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagVARFLAGS
 - oaidl/tagVARFLAGS
 - VARFLAGS
 - oaidl/VARFLAGS
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
 - VARFLAGS
---

# VARFLAGS enumeration


## -description

Specifies variable flags.

## -enum-fields

### -field VARFLAG_FREADONLY:0x1

Assignment to the variable should not be allowed.

### -field VARFLAG_FSOURCE:0x2

The variable returns an object that is a source of events.

### -field VARFLAG_FBINDABLE:0x4

The variable supports data binding.

### -field VARFLAG_FREQUESTEDIT:0x8

When set, any attempt to directly change the property results in a call to <b>IPropertyNotifySink::OnRequestEdit</b>. The implementation of <b>OnRequestEdit</b> determines if the change is accepted.

### -field VARFLAG_FDISPLAYBIND:0x10

The variable is displayed to the user as bindable. VARFLAG_FBINDABLE must also be set.

### -field VARFLAG_FDEFAULTBIND:0x20

The variable is the single property that best represents the object. Only one variable in type information can have this attribute.

### -field VARFLAG_FHIDDEN:0x40

The variable should not be displayed to the user in a browser, although it exists and is bindable.

### -field VARFLAG_FRESTRICTED:0x80

The variable should not be accessible from macro languages. This flag is intended for system-level variables or variables that you do not want type browsers to display.

### -field VARFLAG_FDEFAULTCOLLELEM:0x100

Permits an optimization in which the compiler looks for a member named "xyz" on the type of abc. If such a member is found and is flagged as an accessor function for an element of the default collection, then a call is generated to that member function. Permitted on members in dispinterfaces and interfaces; not permitted on modules.

### -field VARFLAG_FUIDEFAULT:0x200

The variable is the default display in the user interface.

### -field VARFLAG_FNONBROWSABLE:0x400

The variable appears in an object browser, but not in a properties browser.

### -field VARFLAG_FREPLACEABLE:0x800

Tags the interface as having default behaviors.

### -field VARFLAG_FIMMEDIATEBIND:0x1000

The variable is mapped as individual bindable properties.

