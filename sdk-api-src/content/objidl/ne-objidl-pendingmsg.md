---
UID: NE:objidl.tagPENDINGMSG
title: PENDINGMSG (objidl.h)
description: Specifies the return values for the IMessageFilter::MessagePending method.
helpviewer_keywords: ["PENDINGMSG","PENDINGMSG enumeration [COM]","PENDINGMSG_CANCELCALL","PENDINGMSG_WAITDEFPROCESS","PENDINGMSG_WAITNOPROCESS","_com_PENDINGMSG","com.pendingmsg","objidl/PENDINGMSG","objidl/PENDINGMSG_CANCELCALL","objidl/PENDINGMSG_WAITDEFPROCESS","objidl/PENDINGMSG_WAITNOPROCESS"]
old-location: com\pendingmsg.htm
tech.root: com
ms.assetid: 105bbcd4-b1b2-444d-bd55-7f6e564fec42
ms.date: 12/05/2018
ms.keywords: PENDINGMSG, PENDINGMSG enumeration [COM], PENDINGMSG_CANCELCALL, PENDINGMSG_WAITDEFPROCESS, PENDINGMSG_WAITNOPROCESS, _com_PENDINGMSG, com.pendingmsg, objidl/PENDINGMSG, objidl/PENDINGMSG_CANCELCALL, objidl/PENDINGMSG_WAITDEFPROCESS, objidl/PENDINGMSG_WAITNOPROCESS
f1_keywords:
- objidl/PENDINGMSG
dev_langs:
- c++
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
- PENDINGMSG
targetos: Windows
req.typenames: PENDINGMSG
req.redist: 
ms.custom: 19H1
---

# PENDINGMSG enumeration


## -description


Specifies the return values for the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imessagefilter-messagepending">IMessageFilter::MessagePending</a> method.


## -enum-fields




### -field PENDINGMSG_CANCELCALL

Cancel the outgoing call.


### -field PENDINGMSG_WAITNOPROCESS

Wait for the return and don't dispatch the message.


### -field PENDINGMSG_WAITDEFPROCESS

Wait and dispatch the message.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imessagefilter-messagepending">IMessageFilter::MessagePending</a>
 

 

