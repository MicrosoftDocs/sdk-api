---
UID: NE:netlistmgr.NLM_INTERNET_CONNECTIVITY
title: NLM_INTERNET_CONNECTIVITY
author: windows-driver-content
description: The NLM_INTERNET_CONNECTIVITY enumeration defines a set of flags that provide additional data for IPv4 or IPv6 network connectivity.
old-location: nla\nlm_internet_connectivity.htm
old-project: NLA
ms.assetid: 5B1DB4D5-6F69-4628-AEAF-E280E9B4E71C
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: NLM_INTERNET_CONNECTIVITY, NLM_INTERNET_CONNECTIVITY enumeration [Network Awareness], NLM_INTERNET_CONNECTIVITY_CORPORATE, NLM_INTERNET_CONNECTIVITY_PROXIED, NLM_INTERNET_CONNECTIVITY_WEBHIJACK, netlistmgr/NLM_INTERNET_CONNECTIVITY, netlistmgr/NLM_INTERNET_CONNECTIVITY_CORPORATE, netlistmgr/NLM_INTERNET_CONNECTIVITY_PROXIED, netlistmgr/NLM_INTERNET_CONNECTIVITY_WEBHIJACK, nla.nlm_internet_connectivity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: netlistmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Netlistmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NLM_INTERNET_CONNECTIVITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Netlistmgr.h
api_name:
-	NLM_INTERNET_CONNECTIVITY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# NLM_INTERNET_CONNECTIVITY enumeration


## -description


The <b>NLM_INTERNET_CONNECTIVITY</b> enumeration defines a set of flags that provide additional data for IPv4 or IPv6 network connectivity.


## -enum-fields




### -field NLM_INTERNET_CONNECTIVITY_WEBHIJACK

Indicates that the detected network is a hotspot. For example, when connected to a coffee Wi-Fi hotspot network and the local HTTP traffic is being redirected to a captive portal, this flag will be set.


### -field NLM_INTERNET_CONNECTIVITY_PROXIED

Indicates that the detected network has a proxy configuration. For example, when connected to a corporate network using a proxy for HTTP access, this flag will be set.


### -field NLM_INTERNET_CONNECTIVITY_CORPORATE

Indicates that the machine is configured for Direct Access and that access to the corporate domain network, for which Direct Access was previously configured, has been detected.


## -remarks



These connectivity flags can be retrieved by querying  for the <i>NA_InternetConnectivityV4</i> or <i>NA_InternetConnectivityV6</i> properties using the <b>IPropertyBag</b> interface for an <a href="https://msdn.microsoft.com/6d483058-f7c4-4a6c-a1a8-816c2fab9994">INetwork</a> or <a href="https://msdn.microsoft.com/666761b5-0146-438d-9986-ecce3b45b5ff">INetworkConnection</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/6d483058-f7c4-4a6c-a1a8-816c2fab9994">INetwork</a>



<a href="https://msdn.microsoft.com/666761b5-0146-438d-9986-ecce3b45b5ff">INetworkConnection</a>



<a href="com.ipropertybag">IPropertyBag</a>
 

 

