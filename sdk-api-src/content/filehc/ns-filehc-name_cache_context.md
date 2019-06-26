---
UID: NS:filehc.NAME_CACHE_CONTEXT
title: NAME_CACHE_CONTEXT (filehc.h)
author: windows-sdk-content
description: Represents a name cache.
old-location: winprog\name_cache_context.htm
tech.root: DevNotes
ms.assetid: 2d2a6066-b59a-418c-a726-0a1a39243988
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PNAME_CACHE_CONTEXT, NAME_CACHE_CONTEXT, NAME_CACHE_CONTEXT structure [Windows API], PNAME_CACHE_CONTEXT, PNAME_CACHE_CONTEXT structure pointer [Windows API], filehc/NAME_CACHE_CONTEXT, filehc/PNAME_CACHE_CONTEXT, winprog.name_cache_context"
ms.topic: struct
f1_keywords: 
 - "filehc/NAME_CACHE_CONTEXT"
req.header: filehc.h
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
 - Filehc.h
api_name:
 - NAME_CACHE_CONTEXT
product: Windows
targetos: Windows
req.typenames: "*PNAME_CACHE_CONTEXT"
req.redist: 
ms.custom: 19H1
---

# NAME_CACHE_CONTEXT structure


## -description


Represents a name cache. This structure does not contain any fields that are useful to a client, but it must be passed back into all of the name cache APIs.


## -struct-fields




### -field m_dwSignature

The signature to this structure to ensure whether this name cache context is valid.

<div class="alert"><b>Note</b>  Users should never change this for any reason.</div>
<div> </div>
