---
UID: NE:oaidl.tagTYPEFLAGS
title: tagTYPEFLAGS
author: windows-sdk-content
description: The type flags.
old-location: automat\typeflags.htm
old-project: automat
ms.assetid: bf34cc90-f772-4562-9d18-7cf35aeed41e
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: TYPEFLAGS, TYPEFLAGS enumeration [Automation], TYPEFLAG_FAGGREGATABLE, TYPEFLAG_FAPPOBJECT, TYPEFLAG_FCANCREATE, TYPEFLAG_FCONTROL, TYPEFLAG_FDISPATCHABLE, TYPEFLAG_FDUAL, TYPEFLAG_FHIDDEN, TYPEFLAG_FLICENSED, TYPEFLAG_FNONEXTENSIBLE, TYPEFLAG_FOLEAUTOMATION, TYPEFLAG_FPREDECLID, TYPEFLAG_FPROXY, TYPEFLAG_FREPLACEABLE, TYPEFLAG_FRESTRICTED, TYPEFLAG_FREVERSEBIND, _oa96_TYPEFLAGS, automat.typeflags, oaidl/TYPEFLAGS, oaidl/TYPEFLAG_FAGGREGATABLE, oaidl/TYPEFLAG_FAPPOBJECT, oaidl/TYPEFLAG_FCANCREATE, oaidl/TYPEFLAG_FCONTROL, oaidl/TYPEFLAG_FDISPATCHABLE, oaidl/TYPEFLAG_FDUAL, oaidl/TYPEFLAG_FHIDDEN, oaidl/TYPEFLAG_FLICENSED, oaidl/TYPEFLAG_FNONEXTENSIBLE, oaidl/TYPEFLAG_FOLEAUTOMATION, oaidl/TYPEFLAG_FPREDECLID, oaidl/TYPEFLAG_FPROXY, oaidl/TYPEFLAG_FREPLACEABLE, oaidl/TYPEFLAG_FRESTRICTED, oaidl/TYPEFLAG_FREVERSEBIND, tagTYPEFLAGS
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
req.typenames: TYPEFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	OaIdl.h
api_name:
-	TYPEFLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# tagTYPEFLAGS enumeration


## -description


The type flags.


## -enum-fields




### -field TYPEFLAG_FAPPOBJECT

A type description that describes an Application object.


### -field TYPEFLAG_FCANCREATE

Instances of the type can be created by <a href="https://msdn.microsoft.com/b11c51e6-8ae7-482d-87eb-8175ca98eb63">ITypeInfo::CreateInstance</a>.



### -field TYPEFLAG_FLICENSED

The type is licensed.


### -field TYPEFLAG_FPREDECLID

The type is predefined. The client application should automatically create a single instance of the object that has this attribute. The name of the variable that points to the object is the same as the class name of the object.



### -field TYPEFLAG_FHIDDEN

The type should not be displayed to browsers.



### -field TYPEFLAG_FCONTROL

The type is a control from which other types will be derived, and should not be displayed to users.



### -field TYPEFLAG_FDUAL

The interface supplies both <a href="https://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> and VTBL binding. 



### -field TYPEFLAG_FNONEXTENSIBLE

The interface cannot add members at run time.



### -field TYPEFLAG_FOLEAUTOMATION

The types used in the interface are fully compatible with Automation, including VTBL binding support. Setting dual on an interface sets this flag in addition to TYPEFLAG_FDUAL. Not allowed on dispinterfaces.



### -field TYPEFLAG_FRESTRICTED

Should not be accessible from macro languages. This flag is intended for system-level types or types that type browsers should not display.



### -field TYPEFLAG_FAGGREGATABLE

The class supports aggregation.



### -field TYPEFLAG_FREPLACEABLE

The type is replaceable.


### -field TYPEFLAG_FDISPATCHABLE

Indicates that the interface derives from <a href="https://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>, either directly or indirectly. This flag is computed. There is no Object Description Language for the flag.



### -field TYPEFLAG_FREVERSEBIND

The type has reverse binding.


### -field TYPEFLAG_FPROXY

Interfaces can be marked with this flag to indicate that they will be using a proxy/stub dynamic link library. This flag specifies that the typelib proxy should not be unregistered when the typelib is unregistered.



## -remarks



TYPEFLAG_FAPPOBJECT can be used on type descriptions with TypeKind = TKIND_COCLASS, and indicates that the type description specifies an Application object.

Members of the Application object are globally accessible. The <a href="https://msdn.microsoft.com/04814179-2555-4ba5-a08c-bff776c03ca3">Bind</a> method of the <a href="https://msdn.microsoft.com/4d35370f-506f-45cd-9d75-e48c640d8f4d">ITypeComp</a> instance associated with the library binds to the members of an Application object, just as it does for type descriptions that have TypeKind = TKIND_MODULE.



The type description implicitly defines a global variable with the same name and type described by the type description. This variable is also globally accessible. When <a href="https://msdn.microsoft.com/04814179-2555-4ba5-a08c-bff776c03ca3">Bind</a> is passed the name of an Application object, a VARDESC is returned, which describes the implicit variable. The ID of the implicitly created variable is always ID_DEFAULTINST.



The <a href="https://msdn.microsoft.com/b11c51e6-8ae7-482d-87eb-8175ca98eb63">ITypeInfo::CreateInstance</a> function of an Application object type description is called, and then it uses <a href="https://msdn.microsoft.com/a276e30c-6a7f-4cde-9639-21a9f5170b62">GetActiveObject</a> to retrieve the Application object. If <b>GetActiveObject</b> fails because the application is not running, then <b>CreateInstance</b> calls <b>CoCreateInstance</b>, which should start the application.



When TYPEFLAG_FCANCREATE is set, <a href="https://msdn.microsoft.com/b11c51e6-8ae7-482d-87eb-8175ca98eb63">CreateInstance</a> can create an instance of this type. This is true only for component object classes for which a globally unique identifier (GUID) has been specified.



