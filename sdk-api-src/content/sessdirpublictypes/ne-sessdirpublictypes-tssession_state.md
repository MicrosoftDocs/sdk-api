---
UID: NE:sessdirpublictypes._TSSESSION_STATE
title: TSSESSION_STATE (sessdirpublictypes.h)
description: Indicates the state of a session.
helpviewer_keywords: ["STATE_ACTIVE","STATE_CONNECTED","STATE_CONNECTQUERY","STATE_DISCONNECTED","STATE_DOWN","STATE_IDLE","STATE_INIT","STATE_INVALID","STATE_LISTEN","STATE_RESET","STATE_SHADOW","TSSESSION_STATE","TSSESSION_STATE enumeration [Remote Desktop Services]","sessdirpublictypes/STATE_ACTIVE","sessdirpublictypes/STATE_CONNECTED","sessdirpublictypes/STATE_CONNECTQUERY","sessdirpublictypes/STATE_DISCONNECTED","sessdirpublictypes/STATE_DOWN","sessdirpublictypes/STATE_IDLE","sessdirpublictypes/STATE_INIT","sessdirpublictypes/STATE_INVALID","sessdirpublictypes/STATE_LISTEN","sessdirpublictypes/STATE_RESET","sessdirpublictypes/STATE_SHADOW","sessdirpublictypes/TSSESSION_STATE","termserv.tssession_state"]
old-location: termserv\tssession_state.htm
tech.root: TermServ
ms.assetid: 2780e704-72f1-44a9-ad54-ab3d2b19befe
ms.date: 12/05/2018
ms.keywords: STATE_ACTIVE, STATE_CONNECTED, STATE_CONNECTQUERY, STATE_DISCONNECTED, STATE_DOWN, STATE_IDLE, STATE_INIT, STATE_INVALID, STATE_LISTEN, STATE_RESET, STATE_SHADOW, TSSESSION_STATE, TSSESSION_STATE enumeration [Remote Desktop Services], sessdirpublictypes/STATE_ACTIVE, sessdirpublictypes/STATE_CONNECTED, sessdirpublictypes/STATE_CONNECTQUERY, sessdirpublictypes/STATE_DISCONNECTED, sessdirpublictypes/STATE_DOWN, sessdirpublictypes/STATE_IDLE, sessdirpublictypes/STATE_INIT, sessdirpublictypes/STATE_INVALID, sessdirpublictypes/STATE_LISTEN, sessdirpublictypes/STATE_RESET, sessdirpublictypes/STATE_SHADOW, sessdirpublictypes/TSSESSION_STATE, termserv.tssession_state
req.header: sessdirpublictypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SessDirPublicTypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TSSESSION_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TSSESSION_STATE
 - sessdirpublictypes/_TSSESSION_STATE
 - TSSESSION_STATE
 - sessdirpublictypes/TSSESSION_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - SessDirPublicTypes.h
api_name:
 - TSSESSION_STATE
---

# TSSESSION_STATE enumeration


## -description

Indicates the state of a session.

## -enum-fields

### -field STATE_INVALID:-1

The session state is not valid.

### -field STATE_ACTIVE

The user is logged on to WinStation.

### -field STATE_CONNECTED

WinStation is connected to the client (session reconnected).

### -field STATE_CONNECTQUERY

In the process of connecting to the client (session reconnect pending).

### -field STATE_SHADOW

Shadowing another WinStation.

### -field STATE_DISCONNECTED

WinStation is active but the client is disconnected.

### -field STATE_IDLE

Waiting for the client to connect.

### -field STATE_LISTEN

WinStation is listening for a connection.

### -field STATE_RESET

WinStation is being reset (session logged off).

### -field STATE_DOWN

WinStation is down due to error.

### -field STATE_INIT

WinStation is initializing.

### -field STATE_MAX

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession">ITsSbSession</a>
