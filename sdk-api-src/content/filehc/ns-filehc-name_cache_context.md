---
UID: NS:filehc.NAME_CACHE_CONTEXT
title: NAME_CACHE_CONTEXT
author: windows-sdk-content
description: Represents a name cache.
old-location: winprog\name_cache_context.htm
old-project: DevNotes
ms.assetid: 2d2a6066-b59a-418c-a726-0a1a39243988
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: "*PNAME_CACHE_CONTEXT, NAME_CACHE_CONTEXT, NAME_CACHE_CONTEXT structure [Windows API], PNAME_CACHE_CONTEXT, PNAME_CACHE_CONTEXT structure pointer [Windows API], filehc/NAME_CACHE_CONTEXT, filehc/PNAME_CACHE_CONTEXT, winprog.name_cache_context"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: "*PNAME_CACHE_CONTEXT"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Filehc.h
api_name:
-	NAME_CACHE_CONTEXT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# NAME_CACHE_CONTEXT structure


## -description


Represents a name cache. This structure does not contain any fields that are useful to a client, but it must be passed back into all of the name cache APIs.


## -struct-fields




### -field m_dwSignature

The signature to this structure to ensure whether this name cache context is valid.

<div class="alert"><b>Note</b>  Users should never change this for any reason.</div>
<div> </div>
