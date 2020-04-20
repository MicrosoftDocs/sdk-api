---
UID: NF:networkisolation.NetworkIsolationSetAppContainerConfig
title: NetworkIsolationSetAppContainerConfig function (networkisolation.h)
description: Used to set the configuration of one or more app containers.helpviewer_keywords: ["NetworkIsolationSetAppContainerConfig","NetworkIsolationSetAppContainerConfig function [ICS/ICF]","ics.networkisolationsetappcontainerconfig","networkisolation/NetworkIsolationSetAppContainerConfig"]
old-location: ics\networkisolationsetappcontainerconfig.htm
tech.root: ics
ms.assetid: 88f97650-1896-43f9-acfa-f8411ded5cb8
ms.date: 12/05/2018
ms.keywords: NetworkIsolationSetAppContainerConfig, NetworkIsolationSetAppContainerConfig function [ICS/ICF], ics.networkisolationsetappcontainerconfig, networkisolation/NetworkIsolationSetAppContainerConfig
f1_keywords:
- networkisolation/NetworkIsolationSetAppContainerConfig
dev_langs:
- c++
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
- NetworkIsolationSetAppContainerConfig
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NetworkIsolationSetAppContainerConfig function


## -description


The <b>NetworkIsolationSetAppContainerConfig</b> function is used to set the configuration of one or more app containers.


## -parameters




### -param dwNumPublicAppCs [in]

Type: <b>DWORD</b>

The number of app containers in the <b>appContainerSids</b> member.


### -param appContainerSids [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-sid_and_attributes">PSID_AND_ATTRIBUTES</a></b>

The security identifiers (SIDs) of app containers that are allowed to send loopback traffic. Used for debugging purposes.


## -returns



Type: <b>DWORD</b>

Returns ERROR_SUCCESS if successful, or an error value otherwise. 



