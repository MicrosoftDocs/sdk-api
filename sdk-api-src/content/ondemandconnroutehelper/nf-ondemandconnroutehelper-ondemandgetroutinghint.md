---
UID: NF:ondemandconnroutehelper.OnDemandGetRoutingHint
title: OnDemandGetRoutingHint function (ondemandconnroutehelper.h)
description: The OnDemandGetRoutingHint function looks up a destination in the Route Request cache and, if a match is found, return the corresponding Interface ID.
helpviewer_keywords: ["OnDemandGetRoutingHint","OnDemandGetRoutingHint function [Network Awareness]","nla.ondemandgetroutinghint","ondemandconnroutehelper/OnDemandGetRoutingHint"]
old-location: nla\ondemandgetroutinghint.htm
tech.root: nla
ms.assetid: 6B98416F-A196-4015-836B-D6D649CCA9B1
ms.date: 12/05/2018
ms.keywords: OnDemandGetRoutingHint, OnDemandGetRoutingHint function [Network Awareness], nla.ondemandgetroutinghint, ondemandconnroutehelper/OnDemandGetRoutingHint
req.header: ondemandconnroutehelper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OnDemandConnRouteHelper.lib
req.dll: OnDemandConnRouteHelper.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OnDemandGetRoutingHint
 - ondemandconnroutehelper/OnDemandGetRoutingHint
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OnDemandConnRouteHelper.dll
api_name:
 - OnDemandGetRoutingHint
---

# OnDemandGetRoutingHint function


## -description

The <b>OnDemandGetRoutingHint</b> function looks up a destination in the Route Request cache and, if a match is found, return the corresponding Interface ID.

## -parameters

### -param destinationHostName [in]

An PWSTR describing the target host name for a network communication.

### -param interfaceIndex [out]

The interface index of the network adapter to be used for communicating with the target host.

## -returns

This function returns the following to indicate operation results:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
A match was found in the dll cache. The <i>pdwInterfaceIndex</i> will contain the index of the interface to be used to communicate with the target host.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
A match was not found in the dll cache for the specified host name.

</td>
</tr>
</table>

