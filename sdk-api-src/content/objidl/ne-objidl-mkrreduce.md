---
UID: NE:objidl.tagMKREDUCE
title: MKRREDUCE (objidl.h)
description: Specifies how far a moniker should be reduced.
helpviewer_keywords: ["MKRREDUCE","MKRREDUCE enumeration [COM]","MKRREDUCE_ALL","MKRREDUCE_ONE","MKRREDUCE_THROUGHUSER","MKRREDUCE_TOUSER","_com_MKRREDUCE","com.mkrreduce","objidl/MKRREDUCE","objidl/MKRREDUCE_ALL","objidl/MKRREDUCE_ONE","objidl/MKRREDUCE_THROUGHUSER","objidl/MKRREDUCE_TOUSER"]
old-location: com\mkrreduce.htm
tech.root: com
ms.assetid: ab918d0f-18f2-4ab0-805f-aa228c0d6a82
ms.date: 12/05/2018
ms.keywords: MKRREDUCE, MKRREDUCE enumeration [COM], MKRREDUCE_ALL, MKRREDUCE_ONE, MKRREDUCE_THROUGHUSER, MKRREDUCE_TOUSER, _com_MKRREDUCE, com.mkrreduce, objidl/MKRREDUCE, objidl/MKRREDUCE_ALL, objidl/MKRREDUCE_ONE, objidl/MKRREDUCE_THROUGHUSER, objidl/MKRREDUCE_TOUSER
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: MKRREDUCE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMKREDUCE
 - objidl/tagMKREDUCE
 - MKRREDUCE
 - objidl/MKRREDUCE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Objidl.h
api_name:
 - MKRREDUCE
---

# MKRREDUCE enumeration


## -description

Specifies how far a moniker should be reduced.

## -enum-fields

### -field MKRREDUCE_ONE

Performs only one step of reducing the moniker. In general, the caller must have specific knowledge about the particular kind of moniker to take advantage of this option.

### -field MKRREDUCE_TOUSER

Reduces the moniker to a form that the user identifies as a persistent object. If no such point exists, then this option should be treated as MKRREDUCE_ALL.

### -field MKRREDUCE_THROUGHUSER

Reduces the moniker to where any further reduction would reduce it to a form that the user does not identify as a persistent object. Often, this is the same stage as MKRREDUCE_TOUSER.

### -field MKRREDUCE_ALL:0

Reduces the moniker until it is in its simplest form, that is, reduce it to itself.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-imoniker-reduce">IMoniker::Reduce</a>
