---
UID: NF:netfw.NetworkIsolationFreeAppContainers
title: NetworkIsolationFreeAppContainers function (netfw.h)
description: The NetworkIsolationFreeAppContainers function is used to release memory resources allocated to one or more app containers.
helpviewer_keywords: ["NetworkIsolationFreeAppContainers","NetworkIsolationFreeAppContainers function [ICS/ICF]","ics.networkisolationfreeappcontainers","networkisolation/NetworkIsolationFreeAppContainers"]
old-location: ics\networkisolationfreeappcontainers.htm
tech.root: ics
ms.assetid: d850eef3-382e-4b3e-9059-35f3171a07c7
ms.date: 08/02/2022
ms.keywords: NetworkIsolationFreeAppContainers, NetworkIsolationFreeAppContainers function [ICS/ICF], ics.networkisolationfreeappcontainers, networkisolation/NetworkIsolationFreeAppContainers
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
req.dll: Firewallapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetworkIsolationFreeAppContainers
 - netfw/NetworkIsolationFreeAppContainers
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - firewallapi.dll
 - API-MS-Win-Net-Isolation-l1-1-0.dll
 - API-MS-Win-Net-Isolation-l1-1-1.dll
 - wfapihost.dll
api_name:
 - NetworkIsolationFreeAppContainers
---

## -description

The <b>NetworkIsolationFreeAppContainers</b> function is used to release memory resources allocated to one or more app containers

## -parameters

### -param pPublicAppCs [in]

Type: <b><a href="/windows/desktop/api/netfw/ns-netfw-inet_firewall_app_container">PINET_FIREWALL_APP_CONTAINER</a></b>

The app container memory resources to be freed.

## -returns

Type: <b>DWORD</b>

Returns **ERROR_SUCCESS**.

## -see-also

<a href="/windows/desktop/api/netfw/ns-netfw-inet_firewall_app_container">INET_FIREWALL_APP_CONTAINER</a>
