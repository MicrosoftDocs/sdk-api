---
UID: NS:mbnapi.MBN_PROVIDER2
title: MBN_PROVIDER2 (mbnapi.h)
description: The MBN_PROVIDER2 structure represents a network service provider. It is used by many of the provider-specific methods of the IMbnMultiCarrier interface and provides an extension to MBN_PROVIDER to support multi-carrier.
helpviewer_keywords: ["MBN_PROVIDER2","MBN_PROVIDER2 structure [Microsoft Broadband Networks]","mbn.mbn_provider2","mbnapi/MBN_PROVIDER2"]
old-location: mbn\mbn_provider2.htm
tech.root: mbn
ms.assetid: 9D681192-1E40-4314-8E7F-8934AA8162D3
ms.date: 12/05/2018
ms.keywords: MBN_PROVIDER2, MBN_PROVIDER2 structure [Microsoft Broadband Networks], mbn.mbn_provider2, mbnapi/MBN_PROVIDER2
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
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
req.typenames: MBN_PROVIDER2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_PROVIDER2
 - mbnapi/MBN_PROVIDER2
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
 - MBN_PROVIDER2
---

## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_PROVIDER2</b> structure represents a network service provider. It is used by many of the provider-specific methods of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnmulticarrier">IMbnMultiCarrier</a> interface and provides an extension to <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_provider">MBN_PROVIDER</a> to support multi-carrier. This extension contains the signal strength of each provider, which helps to determine which provider a user should connect to.

## -struct-fields

### -field provider

Contains a single-carrier <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_provider">MBN_PROVIDER</a> structure.

### -field cellularClass

Contains a <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_cellular_class">MBN_CELLULAR_CLASS</a> that specifies which cellular class the provider uses.

### -field signalStrength

Contains the signal quality received by the device as defined by <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsignal-getsignalstrength">GetSignalStrength</a>.

### -field signalError

Contains the signal error rate as defined by <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsignal-getsignalerror">GetSignalError</a>.

## -see-also

<a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_provider">MBN_PROVIDER</a>
