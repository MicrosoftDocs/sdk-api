---
UID: NE:oaidl.tagVARFLAGS
title: tagVARFLAGS
author: windows-sdk-content
description: Specifies variable flags.
old-location: automat\varflags.htm
old-project: automat
ms.assetid: 9422f2a5-d8c0-4d65-ad7a-9eaa9bbedf91
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: VARFLAGS, VARFLAGS enumeration [Automation], VARFLAG_FBINDABLE, VARFLAG_FDEFAULTBIND, VARFLAG_FDEFAULTCOLLELEM, VARFLAG_FDISPLAYBIND, VARFLAG_FHIDDEN, VARFLAG_FIMMEDIATEBIND, VARFLAG_FNONBROWSABLE, VARFLAG_FREADONLY, VARFLAG_FREPLACEABLE, VARFLAG_FREQUESTEDIT, VARFLAG_FRESTRICTED, VARFLAG_FSOURCE, VARFLAG_FUIDEFAULT, _oa96_VARFLAGS, automat.varflags, oaidl/VARFLAGS, oaidl/VARFLAG_FBINDABLE, oaidl/VARFLAG_FDEFAULTBIND, oaidl/VARFLAG_FDEFAULTCOLLELEM, oaidl/VARFLAG_FDISPLAYBIND, oaidl/VARFLAG_FHIDDEN, oaidl/VARFLAG_FIMMEDIATEBIND, oaidl/VARFLAG_FNONBROWSABLE, oaidl/VARFLAG_FREADONLY, oaidl/VARFLAG_FREPLACEABLE, oaidl/VARFLAG_FREQUESTEDIT, oaidl/VARFLAG_FRESTRICTED, oaidl/VARFLAG_FSOURCE, oaidl/VARFLAG_FUIDEFAULT, tagVARFLAGS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OAIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VARFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	OaIdl.h
api_name:
-	VARFLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# tagVARFLAGS enumeration


## -description


Specifies variable flags.


## -enum-fields




### -field VARFLAG_FREADONLY

Assignment to the variable should not be allowed.



### -field VARFLAG_FSOURCE

The variable returns an object that is a source of events.



### -field VARFLAG_FBINDABLE

The variable supports data binding.



### -field VARFLAG_FREQUESTEDIT

When set, any attempt to directly change the property results in a call to <b>IPropertyNotifySink::OnRequestEdit</b>. The implementation of <b>OnRequestEdit</b> determines if the change is accepted.



### -field VARFLAG_FDISPLAYBIND

The variable is displayed to the user as bindable. VARFLAG_FBINDABLE must also be set. 



### -field VARFLAG_FDEFAULTBIND

The variable is the single property that best represents the object. Only one variable in type information can have this attribute. 



### -field VARFLAG_FHIDDEN

The variable should not be displayed to the user in a browser, although it exists and is bindable.



### -field VARFLAG_FRESTRICTED

The variable should not be accessible from macro languages. This flag is intended for system-level variables or variables that you do not want type browsers to display.



### -field VARFLAG_FDEFAULTCOLLELEM

Permits an optimization in which the compiler looks for a member named "xyz" on the type of abc. If such a member is found and is flagged as an accessor function for an element of the default collection, then a call is generated to that member function. Permitted on members in dispinterfaces and interfaces; not permitted on modules.



### -field VARFLAG_FUIDEFAULT

The variable is the default display in the user interface.



### -field VARFLAG_FNONBROWSABLE

The variable appears in an object browser, but not in a properties browser.



### -field VARFLAG_FREPLACEABLE

Tags the interface as having default behaviors.



### -field VARFLAG_FIMMEDIATEBIND

The variable is mapped as individual bindable properties.


