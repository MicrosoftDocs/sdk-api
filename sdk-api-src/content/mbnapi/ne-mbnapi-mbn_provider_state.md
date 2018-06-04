---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 



