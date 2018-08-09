---
UID: NE:oaidl.tagVARKIND
title: tagVARKIND
author: windows-sdk-content
description: Specifies the variable type.
old-location: automat\varkind.htm
old-project: automat
ms.assetid: 8b2df767-bba1-4e0a-be63-32d45fb2be07
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: VARKIND, VARKIND enumeration [Automation], VAR_CONST, VAR_DISPATCH, VAR_PERINSTANCE, VAR_STATIC, _oa96_VARKIND, automat.varkind, oaidl/VARKIND, oaidl/VAR_CONST, oaidl/VAR_DISPATCH, oaidl/VAR_PERINSTANCE, oaidl/VAR_STATIC, tagVARKIND
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
req.typenames: VARKIND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OaIdl.h
api_name:
 - VARKIND
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# tagVARKIND enumeration


## -description


Specifies the variable type.


## -enum-fields




### -field VAR_PERINSTANCE

The variable is a field or member of the type. It exists at a fixed offset within each instance of the type.


### -field VAR_STATIC

There is only one instance of the variable.



### -field VAR_CONST

The VARDESC describes a symbolic constant. There is no memory associated with it.



### -field VAR_DISPATCH

The variable can only be accessed through <a href="https://msdn.microsoft.com/964ade8e-9d8a-4d32-bd47-aa678912a54d">IDispatch::Invoke</a>.


