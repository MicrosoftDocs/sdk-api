---
UID: NF:networkisolation.NetworkIsolationSetupAppContainerBinaries
title: NetworkIsolationSetupAppContainerBinaries function (networkisolation.h)
description: The NetworkIsolationSetupAppContainerBinaries function is used by software installers to provide information about the image paths of applications that are running in an app container. 
helpviewer_keywords: ["NetworkIsolationSetupAppContainerBinaries","NetworkIsolationSetupAppContainerBinaries function [ICS/ICF]","ics.networkisolationsetupappcontainerbinaries","networkisolation/NetworkIsolationSetupAppContainerBinaries"]
old-location: ics\networkisolationsetupappcontainerbinaries.htm
tech.root: ics
ms.assetid: 67a183ec-b318-4f43-9241-cc34b9b251f1
ms.date: 08/03/2022
ms.keywords: NetworkIsolationSetupAppContainerBinaries, NetworkIsolationSetupAppContainerBinaries function [ICS/ICF], ics.networkisolationsetupappcontainerbinaries, networkisolation/NetworkIsolationSetupAppContainerBinaries
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
 - NetworkIsolationSetupAppContainerBinaries
 - networkisolation/NetworkIsolationSetupAppContainerBinaries
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
 - NetworkIsolationSetupAppContainerBinaries
---

# NetworkIsolationSetupAppContainerBinaries function


## -description

The <b>NetworkIsolationSetupAppContainerBinaries</b> function is used by software installers to provide information about the image paths of applications that are running in an app container.   This information is provided to third-party firewall applications about the applications in order to enhance user experience and security decisions.

## -parameters

### -param applicationContainerSid [in]

Type: <b>PSID</b>

The package identifier of the app container.

### -param packageFullName [in]

Type: <b>LPCWSTR</b>

A string representing the package identity of the app that owns this app container. Contains the 5-part tuple as individual fields (name, version, architecture, resourceid, publisher).

### -param packageFolder [in]

Type: <b>LPCWSTR</b>

The file location of the app that owns this app container.

### -param displayName [in]

Type: <b>LPCWSTR</b>

The friendly name of the app container.

### -param bBinariesFullyComputed [in]

Type: <b>BOOL</b>

True if the binary files are being provided by the caller; otherwise, false.

### -param binaries [in]

Type: <b>LPCWSTR*</b>

An array of paths to the applications running in the app container.

### -param binariesCount [in]

Type: <b>DWORD</b>

The number of paths contained in the <i>binaries</i> parameter.

## -returns

Type: <b>HRESULT</b>

If the function succeeds, it returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Applications creating an app container can use <b>NetworkIsolationSetupAppContainerBinaries</b> to provide third-party firewall applications with  the direct path to applications running inside that app container.
