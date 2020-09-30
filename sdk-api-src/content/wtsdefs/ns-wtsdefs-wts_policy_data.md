---
UID: NS:wtsdefs._WTS_POLICY_DATA
title: WTS_POLICY_DATA (wtsdefs.h)
description: Contains policy information that is passed by the Remote Desktop Services service to the protocol.
helpviewer_keywords: ["*PWTS_POLICY_DATA","1","2","3","4","5","PWTS_POLICY_DATA","PWTS_POLICY_DATA structure pointer [Remote Desktop Services]","WTS_POLICY_DATA","WTS_POLICY_DATA structure [Remote Desktop Services]","termserv.wts_policy_data","wtsdefs/PWTS_POLICY_DATA","wtsdefs/WTS_POLICY_DATA"]
old-location: termserv\wts_policy_data.htm
tech.root: TermServ
ms.assetid: 407de671-f6e3-407e-9c97-11ea9ac8bdde
ms.date: 12/05/2018
ms.keywords: '*PWTS_POLICY_DATA, 1, 2, 3, 4, 5, PWTS_POLICY_DATA, PWTS_POLICY_DATA structure pointer [Remote Desktop Services], WTS_POLICY_DATA, WTS_POLICY_DATA structure [Remote Desktop Services], termserv.wts_policy_data, wtsdefs/PWTS_POLICY_DATA, wtsdefs/WTS_POLICY_DATA'
req.header: wtsdefs.h
req.include-header: Wtsprotocol.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
req.typenames: WTS_POLICY_DATA, *PWTS_POLICY_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WTS_POLICY_DATA
 - wtsdefs/_WTS_POLICY_DATA
 - PWTS_POLICY_DATA
 - wtsdefs/PWTS_POLICY_DATA
 - WTS_POLICY_DATA
 - wtsdefs/WTS_POLICY_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsdefs.h
api_name:
 - WTS_POLICY_DATA
---

# WTS_POLICY_DATA structure


## -description

Contains policy information that is passed by the Remote Desktop Services service to the protocol.

## -struct-fields

### -field fDisableEncryption

Specifies whether to disable encryption for communication between the client and server.

### -field fDisableAutoReconnect

Specifies whether to disable automatic reconnect of the client.

### -field ColorDepth

Specifies the monitor color depth policy. This can be one of the following values.



#### 1

8 bits per pixel



#### 2

15 bits per pixel



#### 3

16 bits per pixel



#### 4

24 bits per pixel



#### 5

32 bits per pixel

### -field MinEncryptionLevel

Specifies the minimum permitted encryption level.

### -field fDisableCpm

Specifies whether to disable printer mapping.

### -field fDisableCdm

Specifies whether to disable drive mapping.

### -field fDisableCcm

Specifies whether to disable COM communication port mapping.

### -field fDisableLPT

Specifies whether to disable LPT (line print terminal) printer redirection.

### -field fDisableClip

Specifies whether to disable clipboard redirection.

### -field fDisablePNPRedir

Specifies whether to disable Plug and Play redirection.

## -remarks

This structure is used by the following methods:

<ul>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-sendpolicydata">SendPolicyData</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getuserdata">GetUserData</a>
</li>
</ul>