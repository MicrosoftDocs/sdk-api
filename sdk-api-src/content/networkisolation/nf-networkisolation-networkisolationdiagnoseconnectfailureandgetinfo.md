---
UID: NF:networkisolation.NetworkIsolationDiagnoseConnectFailureAndGetInfo
title: NetworkIsolationDiagnoseConnectFailureAndGetInfo function (networkisolation.h)
description: The NetworkIsolationDiagnoseConnectFailureAndGetInfo function gets information about a network isolation connection failure due to a missing capability. 
helpviewer_keywords: ["NetworkIsolationDiagnoseConnectFailureAndGetInfo","NetworkIsolationDiagnoseConnectFailureAndGetInfo function [ICS/ICF]","ics.networkisolationdiagnoseconnectfailureandgetinfo","networkisolation/NetworkIsolationDiagnoseConnectFailureAndGetInfo"]
old-location: ics\networkisolationdiagnoseconnectfailureandgetinfo.htm
tech.root: ics
ms.assetid: fb59b2bb-03c1-472d-bb97-6fd9d5f7169d
ms.date: 08/03/2022
ms.keywords: NetworkIsolationDiagnoseConnectFailureAndGetInfo, NetworkIsolationDiagnoseConnectFailureAndGetInfo function [ICS/ICF], ics.networkisolationdiagnoseconnectfailureandgetinfo, networkisolation/NetworkIsolationDiagnoseConnectFailureAndGetInfo
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetworkIsolationDiagnoseConnectFailureAndGetInfo
 - networkisolation/NetworkIsolationDiagnoseConnectFailureAndGetInfo
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
 - NetworkIsolationDiagnoseConnectFailureAndGetInfo
---

# NetworkIsolationDiagnoseConnectFailureAndGetInfo function


## -description

The <b>NetworkIsolationDiagnoseConnectFailureAndGetInfo</b> function gets information about a network isolation connection failure due to a missing capability. This function can be used to identify the capabilities required to connect to a server.

## -parameters

### -param wszServerName [in]

Type: <b>LPCWSTR</b>

Name (or IP address literal string) of the server to which a connection was attempted.

### -param netIsoError [out]

Type: <b><a href="/windows/desktop/api/networkisolation/ne-networkisolation-netiso_error_type">NETISO_ERROR_TYPE</a>*</b>

The error that has occurred, indicating which network capability was missing and thus caused the failure.

## -returns

Type: <b>DWORD</b>

Returns ERROR_SUCCESS if successful, or an error value otherwise.

## -see-also

<a href="/windows/desktop/api/networkisolation/ne-networkisolation-netiso_error_type">NETISO_ERROR_TYPE</a>
