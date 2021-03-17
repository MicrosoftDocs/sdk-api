---
UID: NS:wtsdefs._WRDS_LISTENER_SETTINGS_1
title: WRDS_LISTENER_SETTINGS_1 (wtsdefs.h)
description: Contains listener settings for a remote session.
helpviewer_keywords: ["*PWRDS_LISTENER_SETTINGS_1","PWRDS_LISTENER_SETTINGS_1","PWRDS_LISTENER_SETTINGS_1 structure pointer [Remote Desktop Services]","WRDS_LISTENER_SETTINGS_1","WRDS_LISTENER_SETTINGS_1 structure [Remote Desktop Services]","termserv.wrds_listener_settings_1","wtsdefs/PWRDS_LISTENER_SETTINGS_1","wtsdefs/WRDS_LISTENER_SETTINGS_1"]
old-location: termserv\wrds_listener_settings_1.htm
tech.root: TermServ
ms.assetid: F8F35CED-16EC-4FBB-A3CA-2A5545A88B4A
ms.date: 12/05/2018
ms.keywords: '*PWRDS_LISTENER_SETTINGS_1, PWRDS_LISTENER_SETTINGS_1, PWRDS_LISTENER_SETTINGS_1 structure pointer [Remote Desktop Services], WRDS_LISTENER_SETTINGS_1, WRDS_LISTENER_SETTINGS_1 structure [Remote Desktop Services], termserv.wrds_listener_settings_1, wtsdefs/PWRDS_LISTENER_SETTINGS_1, wtsdefs/WRDS_LISTENER_SETTINGS_1'
req.header: wtsdefs.h
req.include-header: Wtsprotocol.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
req.typenames: WRDS_LISTENER_SETTINGS_1, *PWRDS_LISTENER_SETTINGS_1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WRDS_LISTENER_SETTINGS_1
 - wtsdefs/_WRDS_LISTENER_SETTINGS_1
 - PWRDS_LISTENER_SETTINGS_1
 - wtsdefs/PWRDS_LISTENER_SETTINGS_1
 - WRDS_LISTENER_SETTINGS_1
 - wtsdefs/WRDS_LISTENER_SETTINGS_1
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
 - WRDS_LISTENER_SETTINGS_1
---

# WRDS_LISTENER_SETTINGS_1 structure


## -description

Contains listener settings for a remote session.

## -struct-fields

### -field MaxProtocolListenerConnectionCount

The maximum number of protocol listener connections allowed. <b>ULONG_MAX</b> specifies the maximum number of connections.

### -field SecurityDescriptorSize.range

### -field SecurityDescriptorSize.range.0

### -field SecurityDescriptorSize.range.16384

### -field pSecurityDescriptor.size_is

### -field pSecurityDescriptor.size_is.SecurityDescriptorSize

### -field SecurityDescriptorSize

The size, in bytes, of the <b>pSecurityDescriptor</b> buffer.

### -field pSecurityDescriptor

The address of a buffer that contains the security descriptor for the protocol listener.

