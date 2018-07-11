---
UID: NF:networkisolation.NetworkIsolationFreeAppContainers
title: NetworkIsolationFreeAppContainers function
author: windows-sdk-content
description: Used to release memory resources allocated to one or more app containers.
old-location: ics\networkisolationfreeappcontainers.htm
old-project: ics
ms.assetid: d850eef3-382e-4b3e-9059-35f3171a07c7
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: NetworkIsolationFreeAppContainers, NetworkIsolationFreeAppContainers function [ICS/ICF], ics.networkisolationfreeappcontainers, networkisolation/NetworkIsolationFreeAppContainers
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: networkisolation.h
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
tech.root: 
req.typenames: NETISO_ERROR_TYPE
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
product: Windows
targetos: Windows
req.lib: 
req.dll: Firewallapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# NetworkIsolationFreeAppContainers function


## -description


The <b>NetworkIsolationFreeAppContainers</b> function is used to release memory resources allocated to one or more app containers


## -parameters




### -param pPublicAppCs [in]

Type: <b><a href="https://msdn.microsoft.com/0567fb66-0511-4c80-9e31-2412507ced97">PINET_FIREWALL_APP_CONTAINER</a></b>

The app container memory resources to be freed.


## -returns



Type: <b>DWORD</b>

Returns ERROR_SUCCESS if successful, or an error value otherwise. 




## -see-also




<a href="https://msdn.microsoft.com/0567fb66-0511-4c80-9e31-2412507ced97">INET_FIREWALL_APP_CONTAINER</a>
 

 

