---
UID: NE:objidl.tagCALLTYPE
title: tagCALLTYPE
author: windows-sdk-content
description: Specifies the call types used by IMessageFilter::HandleInComingCall.
old-location: com\calltype.htm
tech.root: com
ms.assetid: 341d429d-8f45-461f-bc77-36e191faecc2
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CALLTYPE, CALLTYPE enumeration [COM], CALLTYPE_ASYNC, CALLTYPE_ASYNC_CALLPENDING, CALLTYPE_NESTED, CALLTYPE_TOPLEVEL, CALLTYPE_TOPLEVEL_CALLPENDING, _com_CALLTYPE, com.calltype, objidl/CALLTYPE, objidl/CALLTYPE_ASYNC, objidl/CALLTYPE_ASYNC_CALLPENDING, objidl/CALLTYPE_NESTED, objidl/CALLTYPE_TOPLEVEL, objidl/CALLTYPE_TOPLEVEL_CALLPENDING, tagCALLTYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Objidl.h
api_name:
 - CALLTYPE
product: Windows
targetos: Windows
req.typenames: CALLTYPE
req.redist: 
---

# tagCALLTYPE enumeration


## -description


Specifies the call types used by <a href="https://msdn.microsoft.com/7e31b518-ef4f-4bdd-b5c7-e1b16383a5be">IMessageFilter::HandleInComingCall</a>. 



## -enum-fields




### -field CALLTYPE_TOPLEVEL

A top-level call has arrived and the object is not currently waiting for a reply from a previous outgoing call. Calls of this type should always be handled.


### -field CALLTYPE_NESTED

A call has arrived bearing the same logical thread identifier as that of a previous outgoing call for which the object is still awaiting a reply. Calls of this type should always be handled.


### -field CALLTYPE_ASYNC

An asynchronous call has arrived. Calls of this type cannot be rejected. OLE always delivers calls of this type. 


### -field CALLTYPE_TOPLEVEL_CALLPENDING

A new top-level call has arrived with a new logical thread identifier and the object is currently waiting for a reply from a previous outgoing call. Calls of this type may be handled or rejected.


### -field CALLTYPE_ASYNC_CALLPENDING

An asynchronous call has arrived with a new logical thread identifier and the object is currently waiting for a reply from a previous outgoing call. Calls of this type cannot be rejected.



## -see-also




<a href="https://msdn.microsoft.com/7e31b518-ef4f-4bdd-b5c7-e1b16383a5be">IMessageFilter::HandleInComingCall</a>
 

 

