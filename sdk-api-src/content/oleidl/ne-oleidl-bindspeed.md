---
UID: NE:oleidl.tagBINDSPEED
title: BINDSPEED (oleidl.h)
description: Indicates approximately how long the caller will wait to bind to an object.
helpviewer_keywords: ["BINDSPEED","BINDSPEED enumeration [COM]","BINDSPEED_IMMEDIATE","BINDSPEED_INDEFINITE","BINDSPEED_MODERATE","_com_BINDSPEED","com.bindspeed","oleidl/BINDSPEED","oleidl/BINDSPEED_IMMEDIATE","oleidl/BINDSPEED_INDEFINITE","oleidl/BINDSPEED_MODERATE"]
old-location: com\bindspeed.htm
tech.root: com
ms.assetid: d39f662b-60ef-4e84-ae62-14e360a57b4f
ms.date: 12/05/2018
ms.keywords: BINDSPEED, BINDSPEED enumeration [COM], BINDSPEED_IMMEDIATE, BINDSPEED_INDEFINITE, BINDSPEED_MODERATE, _com_BINDSPEED, com.bindspeed, oleidl/BINDSPEED, oleidl/BINDSPEED_IMMEDIATE, oleidl/BINDSPEED_INDEFINITE, oleidl/BINDSPEED_MODERATE
req.header: oleidl.h
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
req.typenames: BINDSPEED
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagBINDSPEED
 - oleidl/tagBINDSPEED
 - BINDSPEED
 - oleidl/BINDSPEED
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Oleidl.h
api_name:
 - BINDSPEED
---

# BINDSPEED enumeration


## -description

Indicates approximately how long the caller will wait to bind to an object.

## -enum-fields

### -field BINDSPEED_INDEFINITE:1

There is no time limit on the binding operation.

### -field BINDSPEED_MODERATE:2

The binding operation must be completed in a moderate amount of time. 

If this flag is specified, the implementation of <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleitemcontainer-getobject">IOleItemContainer::GetObject</a> should return MK_E_EXCEEEDEDDEADLINE unless tone of the following is true:

<ul>
<li>The object is already in the running state.
</li>
<li>The object is a pseudo-object (an object internal to the item container, such as a cell-range in a spreadsheet or a character-range in a word processor).</li>
<li>The object is supported by an in-process server (so it is always in the running state when it is loaded). In this case, <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleitemcontainer-getobject">GetObject</a> should load the designated object, and, if the <a href="/windows/desktop/api/ole2/nf-ole2-oleisrunning">OleIsRunning</a> function indicates that the object is running, return successfully. 
</li>
</ul>

### -field BINDSPEED_IMMEDIATE:3

The caller will wait only a short time. In this case, the binding operation should return MK_E_EXCEEEDEDDEADLINE unless the object is already in the running state or is a pseudo-object.

## -remarks

The system-supplied item moniker implementation is the primary caller of <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleitemcontainer-getobject">IOleItemContainer::GetObject</a>. The <b>BINDSPEED</b> value that it specifies depends on the deadline specified by the caller of the moniker operation. 



The deadline is stored in the <b>dwTickCountDeadline</b> field of the <a href="/windows/desktop/api/objidl/ns-objidl-bind_opts">BIND_OPTS</a> structure in the bind context passed to the moniker operation. This value is based on the return value of the <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-gettickcount">GetTickCount</a> function. If <i>dwTickCountDeadline</i> is zero, indicating no deadline, the item moniker implementation specifies BINDSPEED_INDEFINITE. (This is the default <i>dwTickCountDeadline</i> value for a bind context returned by the <a href="/windows/desktop/api/objbase/nf-objbase-createbindctx">CreateBindCtx</a> function.) If the difference between <i>dwTickCountDeadline</i> and the value returned by <b>GetTickCount</b> is greater than 2500, the item moniker implementation specifies BINDSPEED_MODERATE. If the difference is less than 2500, the item moniker implementation specifies BINDSPEED_IMMEDIATE.

Implementations of <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleitemcontainer-getobject">GetObject</a> can use the <b>BINDSPEED</b> value as a shortcut approximation of the binding deadline, or they can use the <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> instance parameter to determine the exact deadline.

## -see-also

<a href="/windows/desktop/api/objidl/ns-objidl-bind_opts">BIND_OPTS</a>



<a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleitemcontainer-getobject">IOleItemContainer::GetObject</a>
