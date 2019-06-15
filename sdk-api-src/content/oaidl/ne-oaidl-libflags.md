---
UID: NE:oaidl.tagLIBFLAGS
title: LIBFLAGS (oaidl.h)
author: windows-sdk-content
description: Defines flags that apply to type libraries.
old-location: automat\libflags.htm
tech.root: automat
ms.assetid: 2c5ecbaf-ce6c-4be1-a3fa-1066dd6e716d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: LIBFLAGS, LIBFLAGS enumeration [Automation], LIBFLAG_FCONTROL, LIBFLAG_FHASDISKIMAGE, LIBFLAG_FHIDDEN, LIBFLAG_FRESTRICTED, _oa96_LIBFLAGS, automat.libflags, oaidl/LIBFLAGS, oaidl/LIBFLAG_FCONTROL, oaidl/LIBFLAG_FHASDISKIMAGE, oaidl/LIBFLAG_FHIDDEN, oaidl/LIBFLAG_FRESTRICTED
ms.topic: enum
f1_keywords: ["oaidl/LIBFLAGS"]
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
 - LIBFLAGS
product: Windows
targetos: Windows
req.typenames: LIBFLAGS
req.redist: 
ms.custom: 19H1
---

# LIBFLAGS enumeration


## -description


Defines flags that apply to type libraries.


## -enum-fields




### -field LIBFLAG_FRESTRICTED

The type library is restricted, and should not be displayed to users.


### -field LIBFLAG_FCONTROL

The type library describes controls, and should not be displayed in type browsers intended for nonvisual objects.



### -field LIBFLAG_FHIDDEN

The type library should not be displayed to users, although its use is not restricted. Should be used by controls. Hosts should create a new type library that wraps the control with extended properties.


### -field LIBFLAG_FHASDISKIMAGE

The type library has a disk image.

