---
UID: NF:ondemandconnroutehelper.OnDemandGetRoutingHint
title: OnDemandGetRoutingHint function
author: windows-driver-content
description: The OnDemandGetRoutingHint function looks up a destination in the Route Request cache and, if a match is found, return the corresponding Interface ID.
old-location: nla\ondemandgetroutinghint.htm
old-project: NLA
ms.assetid: 6B98416F-A196-4015-836B-D6D649CCA9B1
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: OnDemandGetRoutingHint, OnDemandGetRoutingHint function [Network Awareness], nla.ondemandgetroutinghint, ondemandconnroutehelper/OnDemandGetRoutingHint
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: OLEVERB, *LPOLEVERB
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	OnDemandConnRouteHelper.dll
api_name:
-	OnDemandGetRoutingHint
product: Windows
targetos: Windows
req.lib: OnDemandConnRouteHelper.lib
req.dll: OnDemandConnRouteHelper.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# OnDemandGetRoutingHint function


## -description


The <b>OnDemandGetRoutingHint</b> function looks up a destination in the Route Request cache and, if a match is found, return the corresponding Interface ID.


## -parameters




### -param destinationHostName

TBD


### -param interfaceIndex

TBD




#### - DestinationHostName [in]

An PWSTR describing the target host name for a network communication.


#### - pInterfaceIndex [out]

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
 



