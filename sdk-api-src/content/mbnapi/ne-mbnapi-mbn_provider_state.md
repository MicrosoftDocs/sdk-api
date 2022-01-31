---
UID: NE:mbnapi.MBN_PROVIDER_STATE
title: MBN_PROVIDER_STATE (mbnapi.h)
description: The MBN_PROVIDER_STATE enumerated type specifies the various states with which a provider entry can be tagged.
helpviewer_keywords: ["MBN_PROVIDER_STATE","MBN_PROVIDER_STATE enumeration [Microsoft Broadband Networks]","MBN_PROVIDER_STATE_FORBIDDEN","MBN_PROVIDER_STATE_HOME","MBN_PROVIDER_STATE_NONE","MBN_PROVIDER_STATE_PREFERRED","MBN_PROVIDER_STATE_PREFERRED_MULTICARRIER","MBN_PROVIDER_STATE_REGISTERED","MBN_PROVIDER_STATE_VISIBLE","mbn.mbn_provider_state","mbnapi/MBN_PROVIDER_STATE","mbnapi/MBN_PROVIDER_STATE_FORBIDDEN","mbnapi/MBN_PROVIDER_STATE_HOME","mbnapi/MBN_PROVIDER_STATE_NONE","mbnapi/MBN_PROVIDER_STATE_PREFERRED","mbnapi/MBN_PROVIDER_STATE_PREFERRED_MULTICARRIER","mbnapi/MBN_PROVIDER_STATE_REGISTERED","mbnapi/MBN_PROVIDER_STATE_VISIBLE"]
old-location: mbn\mbn_provider_state.htm
tech.root: mbn
ms.assetid: c9bbda5d-96bc-410c-afac-eba3e5bd23ee
ms.date: 12/05/2018
ms.keywords: MBN_PROVIDER_STATE, MBN_PROVIDER_STATE enumeration [Microsoft Broadband Networks], MBN_PROVIDER_STATE_FORBIDDEN, MBN_PROVIDER_STATE_HOME, MBN_PROVIDER_STATE_NONE, MBN_PROVIDER_STATE_PREFERRED, MBN_PROVIDER_STATE_PREFERRED_MULTICARRIER, MBN_PROVIDER_STATE_REGISTERED, MBN_PROVIDER_STATE_VISIBLE, mbn.mbn_provider_state, mbnapi/MBN_PROVIDER_STATE, mbnapi/MBN_PROVIDER_STATE_FORBIDDEN, mbnapi/MBN_PROVIDER_STATE_HOME, mbnapi/MBN_PROVIDER_STATE_NONE, mbnapi/MBN_PROVIDER_STATE_PREFERRED, mbnapi/MBN_PROVIDER_STATE_PREFERRED_MULTICARRIER, mbnapi/MBN_PROVIDER_STATE_REGISTERED, mbnapi/MBN_PROVIDER_STATE_VISIBLE
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
req.typenames: MBN_PROVIDER_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_PROVIDER_STATE
 - mbnapi/MBN_PROVIDER_STATE
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
 - MBN_PROVIDER_STATE
---

# MBN_PROVIDER_STATE enumeration


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_PROVIDER_STATE</b> enumerated type specifies the various states with which a provider entry can be tagged.   These values are intended to be used together in a bitwise OR combination.

## -enum-fields

### -field MBN_PROVIDER_STATE_NONE:0

Unknown provider state.

### -field MBN_PROVIDER_STATE_HOME:0x1

The provider is a home operator.

### -field MBN_PROVIDER_STATE_FORBIDDEN:0x2

The provider is on the forbidden list.

### -field MBN_PROVIDER_STATE_PREFERRED:0x4

The provider is on the preferred list.

### -field MBN_PROVIDER_STATE_VISIBLE:0x8

The provider is visible.

### -field MBN_PROVIDER_STATE_REGISTERED:0x10

Windows 8 or later: The provider is currently registered by the device.

### -field MBN_PROVIDER_STATE_PREFERRED_MULTICARRIER:0x20

Windows 8 or later: The provider is currently on the preferred multi-carrier list.

## -remarks

The following table provides the valid combinations of values for different operations.

<table>
<tr>
<th>Operation</th>
<th>MBN_PROVIDER_STATE</th>
</tr>
<tr>
<td>Query Home Provider</td>
<td>MBN_PROVIDER_STATE_HOME</td>
</tr>
<tr>
<td rowspan="2">Query Preferred Providers</td>
<td>MBN_PROVIDER_STATE_FORBIDDEN</td>
</tr>
<tr>
<td>MBN_PROVIDER_STATE_PREFERRED</td>
</tr>
<tr>
<td rowspan="4">Query Visible Providers</td>
<td>MBN_PROVIDER_STATE_REGISTERED</td>
</tr>
<tr>
<td>MBN_PROVIDER_STATE_HOME</td>
</tr>
<tr>
<td>MBN_PROVIDER_STATE_PREFERRED</td>
</tr>
<tr>
<td>MBN_PROVIDER_STATE_FORBIDDEN</td>
</tr>
</table>

