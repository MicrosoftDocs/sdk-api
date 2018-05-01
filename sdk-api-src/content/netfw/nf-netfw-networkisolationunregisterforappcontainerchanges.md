---
UID: NF:netfw.NetworkIsolationUnregisterForAppContainerChanges
title: NetworkIsolationUnregisterForAppContainerChanges function
author: windows-driver-content
description: Is used to cancel an app container change registration and stop receiving notifications.
old-location: ics\networkisolationunregisterforappcontainerchanges.htm
old-project: ICS
ms.assetid: 589f416d-058a-4711-863f-74b0dacc63eb
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: NetworkIsolationUnregisterForAppContainerChanges, NetworkIsolationUnregisterForAppContainerChanges function [ICS/ICF], ics.networkisolationunregisterforappcontainerchanges, networkisolation/NetworkIsolationUnregisterForAppContainerChanges
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
-	NetworkIsolationUnregisterForAppContainerChanges
product: Windows
targetos: Windows
req.lib: 
req.dll: Firewallapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# NetworkIsolationUnregisterForAppContainerChanges function


## -description


The <b>NetworkIsolationUnregisterForAppContainerChanges</b> function  is used to cancel an app container change registration and stop receiving notifications. 


## -parameters




### -param registrationObject [in]

Type: <b>HANDLE</b>

Handle to the previously created registration.


## -returns



Type: <b>DWORD</b>

Returns ERROR_SUCCESS if successful, or an error value otherwise. 




## -see-also




<a href="https://msdn.microsoft.com/2affb2a8-224c-4d2d-86e2-f194d3990dbe">NetworkIsolationRegisterForAppContainerChanges</a>
 

 

