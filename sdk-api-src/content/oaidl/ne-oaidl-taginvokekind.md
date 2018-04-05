---
UID: NE:oaidl.tagINVOKEKIND
title: tagINVOKEKIND
author: windows-driver-content
description: Specifies the way a function is invoked.
old-location: automat\invokekind.htm
old-project: automat
ms.assetid: df6d392e-88f9-4d22-b257-fb6de8abd289
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: INVOKEKIND, INVOKEKIND enumeration [Automation], INVOKE_FUNC, INVOKE_PROPERTYGET, INVOKE_PROPERTYPUT, INVOKE_PROPERTYPUTREF, _oa96_INVOKEKIND, automat.invokekind, oaidl/INVOKEKIND, oaidl/INVOKE_FUNC, oaidl/INVOKE_PROPERTYGET, oaidl/INVOKE_PROPERTYPUT, oaidl/INVOKE_PROPERTYPUTREF, tagINVOKEKIND
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: oaidl.h
req.include-header: OleAuto.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OAIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: INVOKEKIND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	OAIdl.h
api_name:
-	INVOKEKIND
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# tagINVOKEKIND enumeration


## -description


Specifies the way a function is invoked.


## -enum-fields




### -field INVOKE_FUNC

The member is called using a normal function invocation syntax.



### -field INVOKE_PROPERTYGET

The function is invoked using a normal property-access syntax.



### -field INVOKE_PROPERTYPUT

The function is invoked using a property value assignment syntax. Syntactically, a typical programming language might represent changing a property in the same way as assignment. For example: object.property : = value.



### -field INVOKE_PROPERTYPUTREF

The function is invoked using a property reference assignment syntax.


## -remarks



In C, value assignment is written as *pobj1 = *pobj2, while reference assignment is written as pobj1 = pobj2. Other languages have other syntactic conventions. A property or data member can support only a value assignment, a reference assignment, or both. The INVOKEKIND enumeration constants are the same constants that are passed to <a href="https://msdn.microsoft.com/964ade8e-9d8a-4d32-bd47-aa678912a54d">IDispatch::Invoke</a> to specify the way in which a function is invoked.




