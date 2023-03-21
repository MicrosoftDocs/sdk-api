---
UID: NF:netfw.NetworkIsolationSetAppContainerConfig
title: NetworkIsolationSetAppContainerConfig function (netfw.h)
description: The NetworkIsolationSetAppContainerConfig function is used to set the configuration of one or more app containers.
helpviewer_keywords: ["NetworkIsolationSetAppContainerConfig","NetworkIsolationSetAppContainerConfig function [ICS/ICF]","ics.networkisolationsetappcontainerconfig","networkisolation/NetworkIsolationSetAppContainerConfig"]
old-location: ics\networkisolationsetappcontainerconfig.htm
tech.root: ics
ms.assetid: 88f97650-1896-43f9-acfa-f8411ded5cb8
ms.date: 08/02/2022
ms.keywords: NetworkIsolationSetAppContainerConfig, NetworkIsolationSetAppContainerConfig function [ICS/ICF], ics.networkisolationsetappcontainerconfig, networkisolation/NetworkIsolationSetAppContainerConfig
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
 - NetworkIsolationSetAppContainerConfig
 - netfw/NetworkIsolationSetAppContainerConfig
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
 - NetworkIsolationSetAppContainerConfig
---

# NetworkIsolationSetAppContainerConfig function


## -description

The <b>NetworkIsolationSetAppContainerConfig</b> function is used to set the configuration of one or more app containers.

## -parameters

### -param dwNumPublicAppCs [in]

Type: <b>DWORD</b>

The number of app containers in the <b>appContainerSids</b> member.

### -param appContainerSids [in]

Type: <b><a href="/windows/desktop/api/winnt/ns-winnt-sid_and_attributes">PSID_AND_ATTRIBUTES</a></b>

The security identifiers (SIDs) of app containers that are allowed to send loopback traffic. Used for debugging purposes.

## -returns

Type: <b>DWORD</b>

Returns ERROR_SUCCESS if successful, or an error value otherwise.

## -remarks

Note that it is the calling program's responsibility to first call the <b>NetworkIsolationGetAppContainerConfig</b> function in order to retrieve and preserve the app container SIDs already configured to send loopback traffic.
