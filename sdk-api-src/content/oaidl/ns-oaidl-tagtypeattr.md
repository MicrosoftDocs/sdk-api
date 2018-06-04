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

# tagTYPEATTR structure


## -description


Contains attributes of a type.


## -struct-fields




### -field guid

The GUID of the type information.


### -field lcid

The locale of member names and documentation strings.


### -field dwReserved

Reserved.


### -field memidConstructor

The constructor ID, or MEMBERID_NIL if none.


### -field memidDestructor

The destructor ID, or MEMBERID_NIL if none.


### -field lpstrSchema

Reserved.


### -field cbSizeInstance

The size of an instance of this type.


### -field typekind

The kind of type.


### -field cFuncs

The number of functions.


### -field cVars

The number of variables or data members.


### -field cImplTypes

The number of implemented interfaces.


### -field cbSizeVft

The size of this type's VTBL.


### -field cbAlignment

The byte alignment for an instance of this type. A value of 0 indicates alignment on the 64K boundary; 1 indicates no special alignment. For other values, <i>n</i> indicates aligned on byte <i>n</i>.



### -field wTypeFlags

The type flags. See <a href="https://msdn.microsoft.com/bf34cc90-f772-4562-9d18-7cf35aeed41e">TYPEFLAGS</a>.


### -field wMajorVerNum

The major version number.


### -field wMinorVerNum

The minor version number.


### -field tdescAlias

If <b>typekind</b> is TKIND_ALIAS, specifies the type for which this type is an alias.


### -field idldescType

The IDL attributes of the described type.

