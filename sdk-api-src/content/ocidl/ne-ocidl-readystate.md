---
UID: NE:ocidl.tagREADYSTATE
title: READYSTATE (ocidl.h)
description: The ReadyState property retrieves the ReadyState of the MSWebDVD object.
helpviewer_keywords: ["READYSTATE","READYSTATE enumeration [DirectShow]","READYSTATE_COMPLETE","READYSTATE_INTERACTIVE","READYSTATE_LOADED","READYSTATE_LOADING","READYSTATE_UNINITIALIZED","ReadyState Property","ReadyStateProperty","dshow.readystate_property","ocidl/READYSTATE_COMPLETE","ocidl/READYSTATE_INTERACTIVE","ocidl/READYSTATE_LOADED","ocidl/READYSTATE_LOADING","ocidl/READYSTATE_UNINITIALIZED","ocidl/tagREADYSTATE","tagREADYSTATE","tagREADYSTATE enumeration [DirectShow]"]
old-location: dshow\readystate_property.htm
tech.root: dshow
ms.assetid: e43b0fa4-4a5a-4492-a6a9-bf271f58e11b
ms.date: 12/05/2018
ms.keywords: READYSTATE, READYSTATE enumeration [DirectShow], READYSTATE_COMPLETE, READYSTATE_INTERACTIVE, READYSTATE_LOADED, READYSTATE_LOADING, READYSTATE_UNINITIALIZED, ReadyState Property, ReadyStateProperty, dshow.readystate_property, ocidl/READYSTATE_COMPLETE, ocidl/READYSTATE_INTERACTIVE, ocidl/READYSTATE_LOADED, ocidl/READYSTATE_LOADING, ocidl/READYSTATE_UNINITIALIZED, ocidl/tagREADYSTATE, tagREADYSTATE, tagREADYSTATE enumeration [DirectShow]
req.header: ocidl.h
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
req.typenames: READYSTATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagREADYSTATE
 - ocidl/tagREADYSTATE
 - READYSTATE
 - ocidl/READYSTATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ocidl.h
api_name:
 - READYSTATE
---

# READYSTATE enumeration


## -description

<div class="alert"><b>Note</b>  This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems. It may be altered or unavailable in subsequent versions.</div><div> </div>The <code>ReadyState</code> property retrieves the ReadyState of the <b>MSWebDVD</b> object.

## -enum-fields

### -field READYSTATE_UNINITIALIZED:0

Default initialization state.

### -field READYSTATE_LOADING:1

Object is loading its properties.

### -field READYSTATE_LOADED:2

Object has been initialized.

### -field READYSTATE_INTERACTIVE:3

Object is interactive, but not all its data is available.

### -field READYSTATE_COMPLETE:4

Object has received all its data.

## -remarks

This property is read-only with no default value.

Returns an integer value representing the control's ReadyState.

Any object embedded in a Web page exposes the <code>ReadyState</code> property.

