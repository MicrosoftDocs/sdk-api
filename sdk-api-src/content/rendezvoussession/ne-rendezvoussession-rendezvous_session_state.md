---
UID: NE:rendezvoussession.__MIDL___MIDL_itf_rendezvoussession_0000_0000_0001
title: RENDEZVOUS_SESSION_STATE (rendezvoussession.h)
author: windows-sdk-content
description: Provides the list of possible state codes of the session invitation.
old-location: remoteassist\remoteassist_RENDEZVOUS_SESSION_STATE.htm
tech.root: remoteassist
ms.assetid: VS|remoteassist|~\remoteassist\reference\enums\rendezvous_session_state.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RENDEZVOUS_SESSION_STATE, RENDEZVOUS_SESSION_STATE enumeration [Remote Assistance], RSS_ACCEPTED, RSS_CANCELLED, RSS_CONNECTED, RSS_DECLINED, RSS_INVITATION, RSS_READY, RSS_TERMINATED, RSS_UNKNOWN, remoteassist.remoteassist_RENDEZVOUS_SESSION_STATE, remoteassist_RENDEZVOUS_SESSION_STATE, rendezvoussession/RENDEZVOUS_SESSION_STATE, rendezvoussession/RSS_ACCEPTED, rendezvoussession/RSS_CANCELLED, rendezvoussession/RSS_CONNECTED, rendezvoussession/RSS_DECLINED, rendezvoussession/RSS_INVITATION, rendezvoussession/RSS_READY, rendezvoussession/RSS_TERMINATED, rendezvoussession/RSS_UNKNOWN
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - RendezvousSession.h
api_name:
 - RENDEZVOUS_SESSION_STATE
product: Windows
targetos: Windows
req.typenames: RENDEZVOUS_SESSION_STATE
req.redist: 
---

# RENDEZVOUS_SESSION_STATE enumeration


## -description


Provides the list of possible state codes of the session invitation. 


## -enum-fields




### -field RSS_UNKNOWN

Unknown response. 


### -field RSS_READY

The session is ready.


### -field RSS_INVITATION

The session is an invitation. 


### -field RSS_ACCEPTED

The session is accepted. 


### -field RSS_CONNECTED

The session is not ready. 


### -field RSS_CANCELLED

The local session canceled. 


### -field RSS_DECLINED

The session is remotely cancelled. 


### -field RSS_TERMINATED

Protocol error. 

