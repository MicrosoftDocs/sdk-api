---
UID: NE:oaidl.tagLIBFLAGS
title: LIBFLAGS (oaidl.h)
description: Defines flags that apply to type libraries.
helpviewer_keywords: ["LIBFLAGS","LIBFLAGS enumeration [Automation]","LIBFLAG_FCONTROL","LIBFLAG_FHASDISKIMAGE","LIBFLAG_FHIDDEN","LIBFLAG_FRESTRICTED","_oa96_LIBFLAGS","automat.libflags","oaidl/LIBFLAGS","oaidl/LIBFLAG_FCONTROL","oaidl/LIBFLAG_FHASDISKIMAGE","oaidl/LIBFLAG_FHIDDEN","oaidl/LIBFLAG_FRESTRICTED"]
old-location: automat\libflags.htm
tech.root: automat
ms.assetid: 2c5ecbaf-ce6c-4be1-a3fa-1066dd6e716d
ms.date: 12/05/2018
ms.keywords: LIBFLAGS, LIBFLAGS enumeration [Automation], LIBFLAG_FCONTROL, LIBFLAG_FHASDISKIMAGE, LIBFLAG_FHIDDEN, LIBFLAG_FRESTRICTED, _oa96_LIBFLAGS, automat.libflags, oaidl/LIBFLAGS, oaidl/LIBFLAG_FCONTROL, oaidl/LIBFLAG_FHASDISKIMAGE, oaidl/LIBFLAG_FHIDDEN, oaidl/LIBFLAG_FRESTRICTED
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
targetos: Windows
req.typenames: LIBFLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagLIBFLAGS
 - oaidl/tagLIBFLAGS
 - LIBFLAGS
 - oaidl/LIBFLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OaIdl.h
api_name:
 - LIBFLAGS
---

# LIBFLAGS enumeration


## -description

Defines flags that apply to type libraries.

## -enum-fields

### -field LIBFLAG_FRESTRICTED:0x1

The type library is restricted, and should not be displayed to users.

### -field LIBFLAG_FCONTROL:0x2

The type library describes controls, and should not be displayed in type browsers intended for nonvisual objects.

### -field LIBFLAG_FHIDDEN:0x4

The type library should not be displayed to users, although its use is not restricted. Should be used by controls. Hosts should create a new type library that wraps the control with extended properties.

### -field LIBFLAG_FHASDISKIMAGE:0x8

The type library has a disk image.

