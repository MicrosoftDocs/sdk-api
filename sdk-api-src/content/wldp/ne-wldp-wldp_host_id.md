---
UID: NE:wldp.WLDP_HOST_ID
tech.root: security
title: WLDP_HOST_ID
ms.date: 08/23/2022
targetos: Windows
description: Identifies the host type of the WLDP caller.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: wldp.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr:  Windows Server 2012 [desktop apps only]
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - wldp.h
api_name:
 - WLDP_HOST_ID
f1_keywords:
 - WLDP_HOST_ID
 - wldp/WLDP_HOST_ID
dev_langs:
 - c++
helpviewer_keywords:
 - WLDP_HOST_ID
---

## -description

Identifies the host type of the WLDP caller.

## -enum-fields

### -field WLDP_HOST_ID_UNKNOWN

The host type is unknown.

### -field WLDP_HOST_ID_GLOBAL

The host type is global policy.

### -field WLDP_HOST_ID_VBA

The host type is VBScript.

### -field WLDP_HOST_ID_WSH

The host type is Windows Script Host.

### -field WLDP_HOST_ID_POWERSHELL

The host type is Windows Powershell.

### -field WLDP_HOST_ID_IE

The host type is Internet Explorer.

### -field WLDP_HOST_ID_MSI

The host type is the Microsoft Windows Installer.

### -field WLDP_HOST_ID_ALL

Catch-all for custom objects without a subject interface package.

### -field WLDP_HOST_ID_MAX

The maximum enumeration value.


## -remarks

## -see-also

