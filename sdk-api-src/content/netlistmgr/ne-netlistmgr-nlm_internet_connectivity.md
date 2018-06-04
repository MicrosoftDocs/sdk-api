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
 

 

