---
UID: NE:oaidl.tagTYPEKIND
title: tagTYPEKIND
author: windows-sdk-content
description: Specifies a type.
old-location: automat\typekind.htm
tech.root: automat
ms.assetid: ea7ae5cf-9572-4174-bfcb-63aabba26ed8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TKIND_ALIAS, TKIND_COCLASS, TKIND_DISPATCH, TKIND_ENUM, TKIND_INTERFACE, TKIND_MAX, TKIND_MODULE, TKIND_RECORD, TKIND_UNION, TYPEKIND, TYPEKIND enumeration [Automation], _oa96_TYPEKIND, automat.typekind, oaidl/TKIND_ALIAS, oaidl/TKIND_COCLASS, oaidl/TKIND_DISPATCH, oaidl/TKIND_ENUM, oaidl/TKIND_INTERFACE, oaidl/TKIND_MAX, oaidl/TKIND_MODULE, oaidl/TKIND_RECORD, oaidl/TKIND_UNION, oaidl/TYPEKIND, tagTYPEKIND
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - OaIdl.h
api_name:
 - TYPEKIND
product: Windows
targetos: Windows
req.typenames: TYPEKIND
req.redist: 
---

# tagTYPEKIND enumeration


## -description


Specifies a type.


## -enum-fields




### -field TKIND_ENUM

A set of enumerators.



### -field TKIND_RECORD

A structure with no methods.



### -field TKIND_MODULE

A module that can only have static functions and data (for example, a DLL).



### -field TKIND_INTERFACE

A type that has virtual and pure functions.



### -field TKIND_DISPATCH

A set of methods and properties that are accessible through <a href="https://msdn.microsoft.com/964ade8e-9d8a-4d32-bd47-aa678912a54d">IDispatch::Invoke</a>. By default, dual interfaces return TKIND_DISPATCH.



### -field TKIND_COCLASS

A set of implemented component object interfaces.



### -field TKIND_ALIAS

A type that is an alias for another type.



### -field TKIND_UNION

A union, all of whose members have an offset of zero.



### -field TKIND_MAX

End of enum marker.

