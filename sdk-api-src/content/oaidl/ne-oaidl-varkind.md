---
UID: NE:oaidl.tagVARKIND
title: VARKIND (oaidl.h)
author: windows-sdk-content
description: Specifies the variable type.
old-location: automat\varkind.htm
tech.root: automat
ms.assetid: 8b2df767-bba1-4e0a-be63-32d45fb2be07
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: VARKIND, VARKIND enumeration [Automation], VAR_CONST, VAR_DISPATCH, VAR_PERINSTANCE, VAR_STATIC, _oa96_VARKIND, automat.varkind, oaidl/VARKIND, oaidl/VAR_CONST, oaidl/VAR_DISPATCH, oaidl/VAR_PERINSTANCE, oaidl/VAR_STATIC
ms.topic: enum
f1_keywords: ["oaidl/VARKIND"]
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
 - VARKIND
product: Windows
targetos: Windows
req.typenames: VARKIND
req.redist: 
ms.custom: 19H1
---

# VARKIND enumeration


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

The variable can only be accessed through <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke">IDispatch::Invoke</a>.


