---
UID: NE:mbnapi.MBN_PROVIDER_STATE
title: MBN_PROVIDER_STATE
author: windows-sdk-content
description: The MBN_PROVIDER_STATE enumerated type specifies the various states with which a provider entry can be tagged.
old-location: mbn\mbn_provider_state.htm
old-project: mbn
ms.assetid: c9bbda5d-96bc-410c-afac-eba3e5bd23ee
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: MBN_PROVIDER_STATE, MBN_PROVIDER_STATE enumeration [Microsoft Broadband Networks], MBN_PROVIDER_STATE_FORBIDDEN, MBN_PROVIDER_STATE_HOME, MBN_PROVIDER_STATE_NONE, MBN_PROVIDER_STATE_PREFERRED, MBN_PROVIDER_STATE_PREFERRED_MULTICARRIER, MBN_PROVIDER_STATE_REGISTERED, MBN_PROVIDER_STATE_VISIBLE, mbn.mbn_provider_state, mbnapi/MBN_PROVIDER_STATE, mbnapi/MBN_PROVIDER_STATE_FORBIDDEN, mbnapi/MBN_PROVIDER_STATE_HOME, mbnapi/MBN_PROVIDER_STATE_NONE, mbnapi/MBN_PROVIDER_STATE_PREFERRED, mbnapi/MBN_PROVIDER_STATE_PREFERRED_MULTICARRIER, mbnapi/MBN_PROVIDER_STATE_REGISTERED, mbnapi/MBN_PROVIDER_STATE_VISIBLE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mbnapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MBN_PROVIDER_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mbnapi.h
api_name:
 - MBN_PROVIDER_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: Mapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# MBN_PROVIDER_STATE enumeration


## -description


The <b>MBN_PROVIDER_STATE</b> enumerated type specifies the various states with which a provider entry can be tagged.   These values are intended to be used together in a bitwise OR combination.


## -enum-fields




### -field MBN_PROVIDER_STATE_NONE

Unknown provider state.


### -field MBN_PROVIDER_STATE_HOME

The provider is a home operator.


### -field MBN_PROVIDER_STATE_FORBIDDEN

The provider is on the forbidden list.


### -field MBN_PROVIDER_STATE_PREFERRED

The provider is on the preferred list.


### -field MBN_PROVIDER_STATE_VISIBLE

The provider is visible.


### -field MBN_PROVIDER_STATE_REGISTERED

Windows 8 or later: The provider is currently registered by the device.


### -field MBN_PROVIDER_STATE_PREFERRED_MULTICARRIER

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
 



