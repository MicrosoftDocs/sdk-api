---
UID: NE:mbnapi.MBN_PROVIDER_CONSTANTS
title: MBN_PROVIDER_CONSTANTS (mbnapi.h)
description: The MBN_PROVIDER_CONSTANTS enumerated type contains values that define the buffer lengths of MBN_PROVIDER members.
helpviewer_keywords: ["MBN_PROVIDERID_LEN","MBN_PROVIDERNAME_LEN","MBN_PROVIDER_CONSTANTS","MBN_PROVIDER_CONSTANTS enumeration [Microsoft Broadband Networks]","mbn.mbn_provider_constants","mbnapi/MBN_PROVIDERID_LEN","mbnapi/MBN_PROVIDERNAME_LEN","mbnapi/MBN_PROVIDER_CONSTANTS"]
old-location: mbn\mbn_provider_constants.htm
tech.root: mbn
ms.assetid: 1cfe230c-16b5-490d-938f-604489a4a936
ms.date: 12/05/2018
ms.keywords: MBN_PROVIDERID_LEN, MBN_PROVIDERNAME_LEN, MBN_PROVIDER_CONSTANTS, MBN_PROVIDER_CONSTANTS enumeration [Microsoft Broadband Networks], mbn.mbn_provider_constants, mbnapi/MBN_PROVIDERID_LEN, mbnapi/MBN_PROVIDERNAME_LEN, mbnapi/MBN_PROVIDER_CONSTANTS
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
req.typenames: MBN_PROVIDER_CONSTANTS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_PROVIDER_CONSTANTS
 - mbnapi/MBN_PROVIDER_CONSTANTS
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
 - MBN_PROVIDER_CONSTANTS
---

# MBN_PROVIDER_CONSTANTS enumeration


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_PROVIDER_CONSTANTS</b> enumerated type contains values that define the buffer lengths of <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_provider">MBN_PROVIDER</a> members.

## -enum-fields

### -field MBN_PROVIDERNAME_LEN:20

The maximum length of the <b>providerName</b> member of the <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_provider">MBN_PROVIDER</a> structure.

### -field MBN_PROVIDERID_LEN:6

The maximum length of the <b>providerID</b> member of the <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_provider">MBN_PROVIDER</a> structure.
