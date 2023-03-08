---
UID: NE:msdrmdefs._DRMGLOBALOPTIONS
title: DRMGLOBALOPTIONS (msdrmdefs.h)
description: Defines values for specifying which protocol is used for the transport protocol and whether the server lockbox is used. This enumeration is used by the DRMSetGlobalOptions function.
helpviewer_keywords: ["DRMGLOBALOPTIONS","DRMGLOBALOPTIONS enumeration [Active Directory Rights Management Services SDK 1.0]","DRMGLOBALOPTIONS_USE_SERVERSECURITYPROCESSOR","DRMGLOBALOPTIONS_USE_WINHTTP","msdrmdefs/DRMGLOBALOPTIONS","msdrmdefs/DRMGLOBALOPTIONS_USE_SERVERSECURITYPROCESSOR","msdrmdefs/DRMGLOBALOPTIONS_USE_WINHTTP","rm.drmglobaloptions"]
old-location: rm\drmglobaloptions.htm
tech.root: rm
ms.assetid: 57debd49-ec1e-432d-baac-2f828aeb4412
ms.date: 12/05/2018
ms.keywords: DRMGLOBALOPTIONS, DRMGLOBALOPTIONS enumeration [Active Directory Rights Management Services SDK 1.0], DRMGLOBALOPTIONS_USE_SERVERSECURITYPROCESSOR, DRMGLOBALOPTIONS_USE_WINHTTP, msdrmdefs/DRMGLOBALOPTIONS, msdrmdefs/DRMGLOBALOPTIONS_USE_SERVERSECURITYPROCESSOR, msdrmdefs/DRMGLOBALOPTIONS_USE_WINHTTP, rm.drmglobaloptions
req.header: msdrmdefs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DRMGLOBALOPTIONS
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
ms.custom: 19H1
f1_keywords:
 - _DRMGLOBALOPTIONS
 - msdrmdefs/_DRMGLOBALOPTIONS
 - DRMGLOBALOPTIONS
 - msdrmdefs/DRMGLOBALOPTIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msdrmdefs.h
api_name:
 - DRMGLOBALOPTIONS
---

# DRMGLOBALOPTIONS enumeration


## -description

>[!Note]
>The AD RMS SDK leveraging functionality exposed by the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, which leverages functionality exposed by the client in Msipc.dll.

The <b>DRMGLOBALOPTIONS</b> enumeration defines values for specifying which protocol is used for the transport protocol and whether the server lockbox is used. This enumeration is used by the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmsetglobaloptions">DRMSetGlobalOptions</a> function.

## -enum-fields

### -field DRMGLOBALOPTIONS_USE_WINHTTP

The WinHTTP protocol is used for the transport protocol. By default, the WinINet protocol is used.

### -field DRMGLOBALOPTIONS_USE_SERVERSECURITYPROCESSOR

The server lockbox is used. For more information, see <a href="/previous-versions/windows/desktop/adrms_sdk/lockboxes">Lockboxes</a>.

## -remarks

Applications cannot toggle between the WinHTTP and WinINet protocols.

WinINet cannot be used under the network service account. If an application will be run under the network service account, the application must specify the <b>DRMGLOBALOPTIONS_USE_WINHTTP</b> option.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-enumerations">AD RMS Enumerations</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmsetglobaloptions">DRMSetGlobalOptions</a>