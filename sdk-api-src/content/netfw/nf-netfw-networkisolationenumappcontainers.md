---
UID: NF:netfw.NetworkIsolationEnumAppContainers
title: NetworkIsolationEnumAppContainers function (netfw.h)
description: The NetworkIsolationEnumAppContainers function enumerates all of the app containers that have been created in the system. 
helpviewer_keywords: ["NetworkIsolationEnumAppContainers","NetworkIsolationEnumAppContainers function [ICS/ICF]","ics.networkisolationenumappcontainers","networkisolation/NetworkIsolationEnumAppContainers"]
old-location: ics\networkisolationenumappcontainers.htm
tech.root: ics
ms.assetid: 9a940eb5-712a-459e-9932-0115fdfb512b
ms.date: 08/02/2022
ms.keywords: NetworkIsolationEnumAppContainers, NetworkIsolationEnumAppContainers function [ICS/ICF], ics.networkisolationenumappcontainers, networkisolation/NetworkIsolationEnumAppContainers
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
 - NetworkIsolationEnumAppContainers
 - netfw/NetworkIsolationEnumAppContainers
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
 - NetworkIsolationEnumAppContainers
---

# NetworkIsolationEnumAppContainers function


## -description

The <b>NetworkIsolationEnumAppContainers</b> function enumerates all of the app containers that have been created in the system.

## -parameters

### -param Flags [in]

Type: <b>DWORD</b>

May be set to <b>NETISO_FLAG_FORCE_COMPUTE_BINARIES</b> to ensure that all binaries are computed before the app container is returned. This flag should be set if the caller requires up-to-date and complete information on app container binaries. If this flag is not set, returned data may be stale or incomplete.


See <a href="/previous-versions/windows/desktop/api/netfw/ne-netfw-netiso_flag">NETISO_FLAG</a> for more information.

### -param pdwNumPublicAppCs [out]

Type: <b>DWORD*</b>

The number of app containers in the <b>ppPublicAppCs</b> member.

### -param ppPublicAppCs [out]

Type: <b><a href="/windows/desktop/api/netfw/ns-netfw-inet_firewall_app_container">PINET_FIREWALL_APP_CONTAINER</a>*</b>

The list of app container structure elements.

## -returns

Type: <b>DWORD</b>

Returns ERROR_SUCCESS if successful, or an error value otherwise. 

ERROR_OUTOFMEMORY will be returned if memory is unavailable.

## -remarks

If no app containers are installed on the system, ERROR_SUCCESS will still be returned (and <i>ppPublicAppCs</i> will be empty).  If ppPublicAppCs is not empty, <a href="https://docs.microsoft.com/en-us/windows/win32/api/netfw/nf-netfw-networkisolationfreeappcontainers">NetworkIsolationFreeAppContainers</a> should be used to free the memory when you are done using it.

## -see-also

<a href="/windows/desktop/api/netfw/ns-netfw-inet_firewall_app_container">INET_FIREWALL_APP_CONTAINER</a>



<a href="/previous-versions/windows/desktop/api/netfw/ne-netfw-netiso_flag">NETISO_FLAG</a>
