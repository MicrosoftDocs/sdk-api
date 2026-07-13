---
UID: NE:rendezvoussession.__MIDL___MIDL_itf_rendezvoussession_0000_0000_0002
title: RENDEZVOUS_SESSION_FLAGS (rendezvoussession.h)
description: Provides the list of possible flags for the session invitation.
helpviewer_keywords: ["RENDEZVOUS_SESSION_FLAGS","RENDEZVOUS_SESSION_FLAGS enumeration [Remote Assistance]","RSF_INVITEE","RSF_INVITER","RSF_NONE","RSF_ORIGINAL_INVITER","RSF_REMOTE_LEGACYSESSION","remoteassist.remoteassist_RENDEZVOUS_SESSION_FLAGS","remoteassist_RENDEZVOUS_SESSION_FLAGS","rendezvoussession/RENDEZVOUS_SESSION_FLAGS","rendezvoussession/RSF_INVITEE","rendezvoussession/RSF_INVITER","rendezvoussession/RSF_NONE","rendezvoussession/RSF_ORIGINAL_INVITER","rendezvoussession/RSF_REMOTE_LEGACYSESSION"]
old-location: remoteassist\remoteassist_RENDEZVOUS_SESSION_FLAGS.htm
tech.root: remoteassist
ms.assetid: VS|remoteassist|~\remoteassist\reference\enums\rendezvous_session_flags.htm
ms.date: 12/05/2018
ms.keywords: RENDEZVOUS_SESSION_FLAGS, RENDEZVOUS_SESSION_FLAGS enumeration [Remote Assistance], RSF_INVITEE, RSF_INVITER, RSF_NONE, RSF_ORIGINAL_INVITER, RSF_REMOTE_LEGACYSESSION, remoteassist.remoteassist_RENDEZVOUS_SESSION_FLAGS, remoteassist_RENDEZVOUS_SESSION_FLAGS, rendezvoussession/RENDEZVOUS_SESSION_FLAGS, rendezvoussession/RSF_INVITEE, rendezvoussession/RSF_INVITER, rendezvoussession/RSF_NONE, rendezvoussession/RSF_ORIGINAL_INVITER, rendezvoussession/RSF_REMOTE_LEGACYSESSION
req.header: rendezvoussession.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RendezvousSession.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RENDEZVOUS_SESSION_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_rendezvoussession_0000_0000_0002
 - rendezvoussession/__MIDL___MIDL_itf_rendezvoussession_0000_0000_0002
 - RENDEZVOUS_SESSION_FLAGS
 - rendezvoussession/RENDEZVOUS_SESSION_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - RendezvousSession.h
api_name:
 - RENDEZVOUS_SESSION_FLAGS
---

# RENDEZVOUS_SESSION_FLAGS enumeration


## -description

Provides the list of possible flags for the session invitation.

## -enum-fields

### -field RSF_NONE:0

No such value.

### -field RSF_INVITER:0x1

The party that sets the session object is the inviter.

### -field RSF_INVITEE:0x2

The party that sets the session object is the recipient.

### -field RSF_ORIGINAL_INVITER:0x4

### -field RSF_REMOTE_LEGACYSESSION:0x8

### -field RSF_REMOTE_WIN7SESSION:0x10

