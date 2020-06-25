---
UID: NS:mbnapi.MBN_PROVIDER
title: MBN_PROVIDER (mbnapi.h)
description: The MBN_PROVIDER structure represents a network service provider.
helpviewer_keywords: ["MBN_PROVIDER","MBN_PROVIDER structure [Microsoft Broadband Networks]","mbn.mbn_provider","mbnapi/MBN_PROVIDER"]
old-location: mbn\mbn_provider.htm
tech.root: mbn
ms.assetid: f4a02ca2-6be4-4843-a657-5d5dde8be623
ms.date: 12/05/2018
ms.keywords: MBN_PROVIDER, MBN_PROVIDER structure [Microsoft Broadband Networks], mbn.mbn_provider, mbnapi/MBN_PROVIDER
f1_keywords:
- mbnapi/MBN_PROVIDER
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- mbnapi.h
api_name:
- MBN_PROVIDER
targetos: Windows
req.typenames: MBN_PROVIDER
req.redist: 
ms.custom: 19H1
---

# MBN_PROVIDER structure


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_PROVIDER</b> structure represents a network service provider.  It is used by many of the provider-specific methods of <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a>.


## -struct-fields




### -field providerID

Contains the provider ID.  For GSM networks, this string is a concatenation of a 3-digit mobile country code (MCC) and a 2- or 3-digit mobile network code (MNC).  For CDMA networks, this string is a 5-digit SID.  The maximum length of this string is defined by <b>MBN_PROVIDERID_LEN</b> from <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/ne-mbnapi-mbn_provider_constants">MBN_PROVIDER_CONSTANTS</a>.  The caller must free this string by calling <a href="https://msdn.microsoft.com/library/ms221481.aspx">SysFreeString</a>.


### -field providerState

Contains a bitwise OR combination of <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/ne-mbnapi-mbn_provider_state">MBN_PROVIDER_STATE</a> values that represent the provider state.


### -field providerName

Contains the provider name.  The contents of this member should be ignored when setting the preferred provider list.  The maximum length of this string is defined by <b>MBN_PROVIDERNAME_LEN</b> from <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/ne-mbnapi-mbn_provider_constants">MBN_PROVIDER_CONSTANTS</a>.  The string can be empty.  The caller must free this string by calling <a href="https://msdn.microsoft.com/library/ms221481.aspx">SysFreeString</a>.  


### -field dataClass

Contains a bitwise OR combination of <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/ne-mbnapi-mbn_data_class">MBN_DATA_CLASS</a> values that indicate which data services are applicable or available for transfer.  This member should be ignored when queried for the home provider.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/ns-mbnapi-mbn_provider2">MBN_PROVIDER2</a>
 

 

