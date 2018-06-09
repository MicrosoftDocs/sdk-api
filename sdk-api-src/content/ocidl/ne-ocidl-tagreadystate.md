---
UID: NE:ocidl.tagREADYSTATE
title: tagREADYSTATE
author: windows-sdk-content
description: The ReadyState property retrieves the ReadyState of the MSWebDVD object.
old-location: dshow\readystate_property.htm
old-project: DirectShow
ms.assetid: e43b0fa4-4a5a-4492-a6a9-bf271f58e11b
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: READYSTATE, READYSTATE enumeration [DirectShow], READYSTATE_COMPLETE, READYSTATE_INTERACTIVE, READYSTATE_LOADED, READYSTATE_LOADING, READYSTATE_UNINITIALIZED, ReadyState Property, ReadyStateProperty, dshow.readystate_property, ocidl/READYSTATE_COMPLETE, ocidl/READYSTATE_INTERACTIVE, ocidl/READYSTATE_LOADED, ocidl/READYSTATE_LOADING, ocidl/READYSTATE_UNINITIALIZED, ocidl/tagREADYSTATE, tagREADYSTATE, tagREADYSTATE enumeration [DirectShow]
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: READYSTATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ocidl.h
api_name:
 - READYSTATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# tagREADYSTATE enumeration


## -description


<div class="alert"><b>Note</b>  This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems. It may be altered or unavailable in subsequent versions.</div><div> </div>The <code>ReadyState</code> property retrieves the ReadyState of the <b>MSWebDVD</b> object.


## -enum-fields




### -field READYSTATE_UNINITIALIZED

Default initialization state.


### -field READYSTATE_LOADING

Object is loading its properties.


### -field READYSTATE_LOADED

Object has been initialized.


### -field READYSTATE_INTERACTIVE

Object is interactive, but not all its data is available.


### -field READYSTATE_COMPLETE

Object has received all its data.


## -remarks



This property is read-only with no default value.

Returns an integer value representing the control's ReadyState.

Any object embedded in a Web page exposes the <code>ReadyState</code> property.



