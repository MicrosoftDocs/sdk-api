---
UID: NE:mbnapi.MBN_VOICE_CALL_STATE
title: MBN_VOICE_CALL_STATE (mbnapi.h)
description: The MBN_VOICE_CALL_STATE enumerated type specifies the current voice call state of the device.
helpviewer_keywords: ["MBN_VOICE_CALL_STATE","MBN_VOICE_CALL_STATE enumeration [Microsoft Broadband Networks]","MBN_VOICE_CALL_STATE_HANGUP","MBN_VOICE_CALL_STATE_IN_PROGRESS","MBN_VOICE_CALL_STATE_NONE","mbn.mbn_voice_call_state","mbnapi/MBN_VOICE_CALL_STATE","mbnapi/MBN_VOICE_CALL_STATE_HANGUP","mbnapi/MBN_VOICE_CALL_STATE_IN_PROGRESS","mbnapi/MBN_VOICE_CALL_STATE_NONE"]
old-location: mbn\mbn_voice_call_state.htm
tech.root: mbn
ms.assetid: 1b94b210-e50f-4d7b-a738-9c372364c4f8
ms.date: 12/05/2018
ms.keywords: MBN_VOICE_CALL_STATE, MBN_VOICE_CALL_STATE enumeration [Microsoft Broadband Networks], MBN_VOICE_CALL_STATE_HANGUP, MBN_VOICE_CALL_STATE_IN_PROGRESS, MBN_VOICE_CALL_STATE_NONE, mbn.mbn_voice_call_state, mbnapi/MBN_VOICE_CALL_STATE, mbnapi/MBN_VOICE_CALL_STATE_HANGUP, mbnapi/MBN_VOICE_CALL_STATE_IN_PROGRESS, mbnapi/MBN_VOICE_CALL_STATE_NONE
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MBN_VOICE_CALL_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_VOICE_CALL_STATE
 - mbnapi/MBN_VOICE_CALL_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mbnapi.h
api_name:
 - MBN_VOICE_CALL_STATE
---

# MBN_VOICE_CALL_STATE enumeration


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_VOICE_CALL_STATE</b> enumerated type specifies the current voice call state of the device.

## -enum-fields

### -field MBN_VOICE_CALL_STATE_NONE:0

Voice call state is unknown.

### -field MBN_VOICE_CALL_STATE_IN_PROGRESS

An active voice call is in progress.

### -field MBN_VOICE_CALL_STATE_HANGUP

No voice call is in progress.

