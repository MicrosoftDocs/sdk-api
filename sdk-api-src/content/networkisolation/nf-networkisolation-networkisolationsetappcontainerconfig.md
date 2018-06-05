---
UID: NF:networkisolation.NetworkIsolationSetAppContainerConfig
title: NetworkIsolationSetAppContainerConfig function
author: windows-sdk-content
description: Used to set the configuration of one or more app containers.
old-location: ics\networkisolationsetappcontainerconfig.htm
old-project: ICS
ms.assetid: 88f97650-1896-43f9-acfa-f8411ded5cb8
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: NetworkIsolationSetAppContainerConfig, NetworkIsolationSetAppContainerConfig function [ICS/ICF], ics.networkisolationsetappcontainerconfig, networkisolation/NetworkIsolationSetAppContainerConfig
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
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	firewallapi.dll
-	API-MS-Win-Net-Isolation-l1-1-0.dll
-	API-MS-Win-Net-Isolation-l1-1-1.dll
-	wfapihost.dll
api_name:
-	NetworkIsolationSetAppContainerConfig
product: Windows
targetos: Windows
req.lib: 
req.dll: Firewallapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# NetworkIsolationSetAppContainerConfig function


## -description


The <b>NetworkIsolationSetAppContainerConfig</b> function is used to set the configuration of one or more app containers.


## -parameters




### -param dwNumPublicAppCs [in]

Type: <b>DWORD</b>

The number of app containers in the <b>appContainerSids</b> member.


### -param appContainerSids [in]

Type: <b><a href="https://msdn.microsoft.com/d15d5a3f-6b38-4b92-b59c-ff0d27d111d9">PSID_AND_ATTRIBUTES</a></b>

The security identifiers (SIDs) of app containers that are allowed to send loopback traffic. Used for debugging purposes.


## -returns



Type: <b>DWORD</b>

Returns ERROR_SUCCESS if successful, or an error value otherwise. 



