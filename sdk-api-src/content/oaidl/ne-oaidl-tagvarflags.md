---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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


