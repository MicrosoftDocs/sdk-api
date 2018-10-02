---
UID: NF:netfw.NetworkIsolationEnumAppContainers
title: NetworkIsolationEnumAppContainers function
author: windows-sdk-content
description: Enumerates all of the app containers that have been created in the system.
old-location: ics\networkisolationenumappcontainers.htm
tech.root: ICS
ms.assetid: 9a940eb5-712a-459e-9932-0115fdfb512b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: NetworkIsolationEnumAppContainers, NetworkIsolationEnumAppContainers function [ICS/ICF], ics.networkisolationenumappcontainers, networkisolation/NetworkIsolationEnumAppContainers
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NetworkIsolationEnumAppContainers function


## -description


The <b>NetworkIsolationEnumAppContainers</b> function enumerates all of the app containers that have been created in the system.


## -parameters




### -param Flags [in]

Type: <b>DWORD</b>

May be set to <b>NETISO_FLAG_FORCE_COMPUTE_BINARIES</b> to ensure that all binaries are computed before the app container is returned. This flag should be set if the caller requires up-to-date and complete information on app container binaries. If this flag is not set, returned data may be stale or incomplete.


See <a href="https://msdn.microsoft.com/0e07c3ed-0561-453d-b92a-cd0db07ea5cf">NETISO_FLAG</a> for more information.


### -param pdwNumPublicAppCs [out]

Type: <b>DWORD*</b>

The number of app containers in the <b>ppPublicAppCs</b> member.


### -param ppPublicAppCs [out]

Type: <b><a href="https://msdn.microsoft.com/0567fb66-0511-4c80-9e31-2412507ced97">PINET_FIREWALL_APP_CONTAINER</a>*</b>

The list of app container structure elements.


## -returns



Type: <b>DWORD</b>

Returns ERROR_SUCCESS if successful, or an error value otherwise. 

ERROR_OUTOFMEMORY will be returned if memory is unavailable.




## -remarks



If no app containers are installed on the system, ERROR_SUCCESS will still be returned (and <i>ppPublicAppCs</i> will be empty).




## -see-also




<a href="https://msdn.microsoft.com/0567fb66-0511-4c80-9e31-2412507ced97">INET_FIREWALL_APP_CONTAINER</a>



<a href="https://msdn.microsoft.com/0e07c3ed-0561-453d-b92a-cd0db07ea5cf">NETISO_FLAG</a>
 

 

