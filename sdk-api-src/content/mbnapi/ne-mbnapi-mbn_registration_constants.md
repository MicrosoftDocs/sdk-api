---
UID: NE:mbnapi.MBN_REGISTRATION_CONSTANTS
title: MBN_REGISTRATION_CONSTANTS (mbnapi.h)
description: The MBN_REGISTRATION_CONSTANTS enumerated type contains specific values used by IMbnRegistration interface operations.
helpviewer_keywords: ["MBN_CDMA_DEFAULT_PROVIDER_ID","MBN_REGISTRATION_CONSTANTS","MBN_REGISTRATION_CONSTANTS enumeration [Microsoft Broadband Networks]","MBN_ROAMTEXT_LEN","mbn.mbn_registration_constants","mbnapi/MBN_CDMA_DEFAULT_PROVIDER_ID","mbnapi/MBN_REGISTRATION_CONSTANTS","mbnapi/MBN_ROAMTEXT_LEN"]
old-location: mbn\mbn_registration_constants.htm
tech.root: mbn
ms.assetid: d4b0aa6b-899c-493c-9822-92c2710006e4
ms.date: 12/05/2018
ms.keywords: MBN_CDMA_DEFAULT_PROVIDER_ID, MBN_REGISTRATION_CONSTANTS, MBN_REGISTRATION_CONSTANTS enumeration [Microsoft Broadband Networks], MBN_ROAMTEXT_LEN, mbn.mbn_registration_constants, mbnapi/MBN_CDMA_DEFAULT_PROVIDER_ID, mbnapi/MBN_REGISTRATION_CONSTANTS, mbnapi/MBN_ROAMTEXT_LEN
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MBN_REGISTRATION_CONSTANTS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_REGISTRATION_CONSTANTS
 - mbnapi/MBN_REGISTRATION_CONSTANTS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mbnapi.h
api_name:
 - MBN_REGISTRATION_CONSTANTS
---

# MBN_REGISTRATION_CONSTANTS enumeration


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_REGISTRATION_CONSTANTS</b> enumerated type contains specific values used by <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistration">IMbnRegistration</a> interface operations.

## -enum-fields

### -field MBN_ROAMTEXT_LEN:64

The maximum string size of the <i>roamingText</i> parameter in the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistration-getroamingtext">GetRoamingText</a> method of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistration">IMbnRegistration</a> interface.

### -field MBN_CDMA_DEFAULT_PROVIDER_ID:0

Indicates an unknown provider ID in the <i>providerID</i> parameter in the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistration-getproviderid">GetProviderID</a> method of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistration">IMbnRegistration</a> interface.
