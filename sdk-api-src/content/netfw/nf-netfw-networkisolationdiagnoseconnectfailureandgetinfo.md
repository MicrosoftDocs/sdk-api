---
UID: NF:netfw.NetworkIsolationDiagnoseConnectFailureAndGetInfo
title: NetworkIsolationDiagnoseConnectFailureAndGetInfo function
author: windows-sdk-content
description: Gets information about a network isolation connection failure due to a missing capability.
old-location: ics\networkisolationdiagnoseconnectfailureandgetinfo.htm
old-project: ics
ms.assetid: fb59b2bb-03c1-472d-bb97-6fd9d5f7169d
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: NetworkIsolationDiagnoseConnectFailureAndGetInfo, NetworkIsolationDiagnoseConnectFailureAndGetInfo function [ICS/ICF], ics.networkisolationdiagnoseconnectfailureandgetinfo, networkisolation/NetworkIsolationDiagnoseConnectFailureAndGetInfo
ms.prod: windows
ms.technology: windows-sdk
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
 - NetworkIsolationDiagnoseConnectFailureAndGetInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: Firewallapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# NetworkIsolationDiagnoseConnectFailureAndGetInfo function


## -description


The <b>NetworkIsolationDiagnoseConnectFailureAndGetInfo</b> function gets information about a network isolation connection failure due to a missing capability. This function can be used to identify the capabilities required to connect to a server.


## -parameters




### -param wszServerName [in]

Type: <b>LPCWSTR</b>

Name (or IP address literal string) of the server to which a connection was attempted.


### -param netIsoError [out]

Type: <b><a href="https://msdn.microsoft.com/0daa9d07-8a65-4254-b197-a37e6e04ce32">NETISO_ERROR_TYPE</a>*</b>

The error that has occurred, indicating which network capability was missing and thus caused the failure.


## -returns



Type: <b>DWORD</b>

Returns ERROR_SUCCESS if successful, or an error value otherwise. 




## -see-also




<a href="https://msdn.microsoft.com/0daa9d07-8a65-4254-b197-a37e6e04ce32">NETISO_ERROR_TYPE</a>
 

 

