---
UID: NS:netfw._INET_FIREWALL_APP_CONTAINER
title: INET_FIREWALL_APP_CONTAINER (netfw.h)
description: The INET_FIREWALL_APP_CONTAINER structure contains information about a specific app container. (INET_FIREWALL_APP_CONTAINER)
helpviewer_keywords: ["*PINET_FIREWALL_APP_CONTAINER","INET_FIREWALL_APP_CONTAINER","INET_FIREWALL_APP_CONTAINER structure [ICS/ICF]","PINET_FIREWALL_APP_CONTAINER","PINET_FIREWALL_APP_CONTAINER structure pointer [ICS/ICF]","_INET_FIREWALL_APP_CONTAINER","ics.inet_firewall_app_container","networkisolation/INET_FIREWALL_APP_CONTAINER","networkisolation/PINET_FIREWALL_APP_CONTAINER"]
old-location: ics\inet_firewall_app_container.htm
tech.root: ics
ms.assetid: 0567fb66-0511-4c80-9e31-2412507ced97
ms.date: 08/02/2022
ms.keywords: '*PINET_FIREWALL_APP_CONTAINER, INET_FIREWALL_APP_CONTAINER, INET_FIREWALL_APP_CONTAINER structure [ICS/ICF], PINET_FIREWALL_APP_CONTAINER, PINET_FIREWALL_APP_CONTAINER structure pointer [ICS/ICF], _INET_FIREWALL_APP_CONTAINER, ics.inet_firewall_app_container, networkisolation/INET_FIREWALL_APP_CONTAINER, networkisolation/PINET_FIREWALL_APP_CONTAINER'
req.header: netfw.h
req.include-header: Netfw.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: INET_FIREWALL_APP_CONTAINER, *PINET_FIREWALL_APP_CONTAINER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _INET_FIREWALL_APP_CONTAINER
 - netfw/_INET_FIREWALL_APP_CONTAINER
 - PINET_FIREWALL_APP_CONTAINER
 - netfw/PINET_FIREWALL_APP_CONTAINER
 - INET_FIREWALL_APP_CONTAINER
 - netfw/INET_FIREWALL_APP_CONTAINER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - networkisolation.h
api_name:
 - INET_FIREWALL_APP_CONTAINER
---

# INET_FIREWALL_APP_CONTAINER structure


## -description

The <b>INET_FIREWALL_APP_CONTAINER</b> structure contains information about a specific app container.
<div class="code"></div>

## -struct-fields

### -field appContainerSid

Type: <b>SID*</b>

The package identifier of the app container

### -field userSid

Type: <b>SID*</b>

The security identifier (SID) of the user to whom the app container belongs.

### -field appContainerName

Type: <b>LPWSTR</b>

The app container's globally unique name.

 Also referred to as the  Package Family Name, for the app container of a Windows Store app.

### -field displayName

Type: <b>LPWSTR</b>

Friendly name of the app container

### -field description

Type: <b>LPWSTR</b>

A description of the app container (its use, the objective of the application that uses it, etc.)

### -field capabilities

Type: <b><a href="/windows/desktop/api/networkisolation/ns-networkisolation-inet_firewall_ac_capabilities">INET_FIREWALL_AC_CAPABILITIES</a></b>

The capabilities of the app container.

### -field binaries

Type: <b><a href="/windows/desktop/api/netfw/ns-netfw-inet_firewall_ac_binaries">INET_FIREWALL_AC_BINARIES</a></b>

Binary paths to the applications running in the app container.

### -field workingDirectory

### -field packageFullName

## -see-also

<a href="/windows/desktop/api/netfw/ns-netfw-inet_firewall_ac_binaries">INET_FIREWALL_AC_BINARIES</a>



<a href="/windows/desktop/api/networkisolation/ns-networkisolation-inet_firewall_ac_capabilities">INET_FIREWALL_AC_CAPABILITIES</a>
