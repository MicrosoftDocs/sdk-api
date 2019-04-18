---
UID: NF:networkisolation.NetworkIsolationUnregisterForAppContainerChanges
title: NetworkIsolationUnregisterForAppContainerChanges function (networkisolation.h)
author: windows-sdk-content
description: Is used to cancel an app container change registration and stop receiving notifications.
old-location: ics\networkisolationunregisterforappcontainerchanges.htm
tech.root: ics
ms.assetid: 589f416d-058a-4711-863f-74b0dacc63eb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NetworkIsolationUnregisterForAppContainerChanges, NetworkIsolationUnregisterForAppContainerChanges function [ICS/ICF], ics.networkisolationunregisterforappcontainerchanges, networkisolation/NetworkIsolationUnregisterForAppContainerChanges
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
 - NetworkIsolationUnregisterForAppContainerChanges
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
 

 

