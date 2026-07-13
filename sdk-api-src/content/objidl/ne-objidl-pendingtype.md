---
UID: NE:objidl.tagPENDINGTYPE
title: PENDINGTYPE (objidl.h)
description: Indicates the level of nesting in the IMessageFilter::MessagePending method.
helpviewer_keywords: ["PENDINGTYPE","PENDINGTYPE enumeration [COM]","PENDINGTYPE_NESTED","PENDINGTYPE_TOPLEVEL","_com_PENDINGTYPE","com.pendingtype","objidl/PENDINGTYPE","objidl/PENDINGTYPE_NESTED","objidl/PENDINGTYPE_TOPLEVEL"]
old-location: com\pendingtype.htm
tech.root: com
ms.assetid: 8f167342-5398-4ecc-9b56-dcf2b4248c65
ms.date: 12/05/2018
ms.keywords: PENDINGTYPE, PENDINGTYPE enumeration [COM], PENDINGTYPE_NESTED, PENDINGTYPE_TOPLEVEL, _com_PENDINGTYPE, com.pendingtype, objidl/PENDINGTYPE, objidl/PENDINGTYPE_NESTED, objidl/PENDINGTYPE_TOPLEVEL
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
req.typenames: PENDINGTYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPENDINGTYPE
 - objidl/tagPENDINGTYPE
 - PENDINGTYPE
 - objidl/PENDINGTYPE
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
 - PENDINGTYPE
---

# PENDINGTYPE enumeration


## -description

Indicates the level of nesting in the <a href="/windows/desktop/api/objidl/nf-objidl-imessagefilter-messagepending">IMessageFilter::MessagePending</a> method.

## -enum-fields

### -field PENDINGTYPE_TOPLEVEL:1

Top-level call.

### -field PENDINGTYPE_NESTED:2

Nested call.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-imessagefilter-messagepending">IMessageFilter::MessagePending</a>
