---
UID: NE:oaidl.tagFUNCFLAGS
title: tagFUNCFLAGS
author: windows-sdk-content
description: Specifies function flags.
old-location: automat\funcflags.htm
old-project: automat
ms.assetid: 290f8769-dde4-47b9-b3bb-680efc95f532
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: FUNCFLAGS, FUNCFLAGS enumeration [Automation], FUNCFLAG_FBINDABLE, FUNCFLAG_FDEFAULTBIND, FUNCFLAG_FDEFAULTCOLLELEM, FUNCFLAG_FDISPLAYBIND, FUNCFLAG_FHIDDEN, FUNCFLAG_FIMMEDIATEBIND, FUNCFLAG_FNONBROWSABLE, FUNCFLAG_FREPLACEABLE, FUNCFLAG_FREQUESTEDIT, FUNCFLAG_FRESTRICTED, FUNCFLAG_FSOURCE, FUNCFLAG_FUIDEFAULT, FUNCFLAG_FUSESGETLASTERROR, _oa96_FUNCFLAGS, automat.funcflags, oaidl/FUNCFLAGS, oaidl/FUNCFLAG_FBINDABLE, oaidl/FUNCFLAG_FDEFAULTBIND, oaidl/FUNCFLAG_FDEFAULTCOLLELEM, oaidl/FUNCFLAG_FDISPLAYBIND, oaidl/FUNCFLAG_FHIDDEN, oaidl/FUNCFLAG_FIMMEDIATEBIND, oaidl/FUNCFLAG_FNONBROWSABLE, oaidl/FUNCFLAG_FREPLACEABLE, oaidl/FUNCFLAG_FREQUESTEDIT, oaidl/FUNCFLAG_FRESTRICTED, oaidl/FUNCFLAG_FSOURCE, oaidl/FUNCFLAG_FUIDEFAULT, oaidl/FUNCFLAG_FUSESGETLASTERROR, tagFUNCFLAGS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: oaidl.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: FUNCFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OaIdl.h
api_name:
 - FUNCFLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# tagFUNCFLAGS enumeration


## -description


Specifies function flags.


## -enum-fields




### -field FUNCFLAG_FRESTRICTED

The function should not be accessible from macro languages. This flag is intended for system-level functions or functions that type browsers should not display.


### -field FUNCFLAG_FSOURCE

The function returns an object that is a source of events.



### -field FUNCFLAG_FBINDABLE

The function that supports data binding.



### -field FUNCFLAG_FREQUESTEDIT

When set, any call to a method that sets the property results first in a call to <b>IPropertyNotifySink::OnRequestEdit</b>. The implementation of <b>OnRequestEdit</b> determines if the call is allowed to set the property.



### -field FUNCFLAG_FDISPLAYBIND

The function that is displayed to the user as bindable. FUNC_FBINDABLE must also be set.


### -field FUNCFLAG_FDEFAULTBIND

The function that best represents the object. Only one function in a type information can have this attribute.


### -field FUNCFLAG_FHIDDEN

The function should not be displayed to the user, although it exists and is bindable.



### -field FUNCFLAG_FUSESGETLASTERROR

The function supports <b>GetLastError</b>. If an error occurs during the function, the caller can call <b>GetLastError</b> to retrieve the error code.



### -field FUNCFLAG_FDEFAULTCOLLELEM

Permits an optimization in which the compiler looks for a member named xyz on the type of abc. If such a member is found and is flagged as an accessor function for an element of the default collection, then a call is generated to that member function. Permitted on members in dispinterfaces and interfaces; not permitted on modules. For more information, refer to defaultcollelem in Type Libraries and the Object Description Language. 



### -field FUNCFLAG_FUIDEFAULT

The type information member is the default member for display in the user interface.



### -field FUNCFLAG_FNONBROWSABLE

The property appears in an object browser, but not in a properties browser.


### -field FUNCFLAG_FREPLACEABLE

Tags the interface as having default behaviors.


### -field FUNCFLAG_FIMMEDIATEBIND

Mapped as individual bindable properties.


## -remarks



FUNCFLAG_FHIDDEN means that the property should never be shown in object browsers, property browsers, and so on. This function is useful for removing items from an object model. Code can bind to the member, but the user will never know that the member exists.

FUNCFLAG_FNONBROWSABLE means that the property should not be displayed in a properties browser. It is used in circumstances in which an error would occur if the property were shown in a properties browser.

FUNCFLAG_FRESRICTED means that macro-oriented programmers should not be allowed to access this member. These members are usually treated as _FHIDDEN by tools such as Visual Basic, with the main difference being that code cannot bind to those members.



