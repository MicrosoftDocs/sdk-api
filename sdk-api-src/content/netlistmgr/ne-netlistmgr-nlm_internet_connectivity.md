---
UID: NE:netlistmgr.NLM_INTERNET_CONNECTIVITY
title: NLM_INTERNET_CONNECTIVITY (netlistmgr.h)
description: The NLM_INTERNET_CONNECTIVITY enumeration defines a set of flags that provide additional data for IPv4 or IPv6 network connectivity.
helpviewer_keywords: ["NLM_INTERNET_CONNECTIVITY","NLM_INTERNET_CONNECTIVITY enumeration [Network Awareness]","NLM_INTERNET_CONNECTIVITY_CORPORATE","NLM_INTERNET_CONNECTIVITY_PROXIED","NLM_INTERNET_CONNECTIVITY_WEBHIJACK","netlistmgr/NLM_INTERNET_CONNECTIVITY","netlistmgr/NLM_INTERNET_CONNECTIVITY_CORPORATE","netlistmgr/NLM_INTERNET_CONNECTIVITY_PROXIED","netlistmgr/NLM_INTERNET_CONNECTIVITY_WEBHIJACK","nla.nlm_internet_connectivity"]
old-location: nla\nlm_internet_connectivity.htm
tech.root: nla
ms.assetid: 5B1DB4D5-6F69-4628-AEAF-E280E9B4E71C
ms.date: 12/05/2018
ms.keywords: NLM_INTERNET_CONNECTIVITY, NLM_INTERNET_CONNECTIVITY enumeration [Network Awareness], NLM_INTERNET_CONNECTIVITY_CORPORATE, NLM_INTERNET_CONNECTIVITY_PROXIED, NLM_INTERNET_CONNECTIVITY_WEBHIJACK, netlistmgr/NLM_INTERNET_CONNECTIVITY, netlistmgr/NLM_INTERNET_CONNECTIVITY_CORPORATE, netlistmgr/NLM_INTERNET_CONNECTIVITY_PROXIED, netlistmgr/NLM_INTERNET_CONNECTIVITY_WEBHIJACK, nla.nlm_internet_connectivity
f1_keywords:
- netlistmgr/NLM_INTERNET_CONNECTIVITY
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Netlistmgr.h
api_name:
- NLM_INTERNET_CONNECTIVITY
targetos: Windows
req.typenames: NLM_INTERNET_CONNECTIVITY
req.redist: 
ms.custom: 19H1
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



These connectivity flags can be retrieved by querying  for the <i>NA_InternetConnectivityV4</i> or <i>NA_InternetConnectivityV6</i> properties using the <b>IPropertyBag</b> interface for an <a href="/windows/win32/api/netlistmgr/nn-netlistmgr-inetwork">INetwork</a> or <a href="/windows/win32/api/netlistmgr/nn-netlistmgr-inetworkconnection">INetworkConnection</a> interface.




## -see-also




<a href="/windows/win32/api/netlistmgr/nn-netlistmgr-inetwork">INetwork</a>



<a href="/windows/win32/api/netlistmgr/nn-netlistmgr-inetworkconnection">INetworkConnection</a>



<a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)">IPropertyBag</a>
 

 

