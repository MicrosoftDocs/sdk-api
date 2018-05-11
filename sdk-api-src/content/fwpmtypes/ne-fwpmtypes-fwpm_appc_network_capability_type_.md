---
UID: NE:fwpmtypes.FWPM_APPC_NETWORK_CAPABILITY_TYPE_
title: FWPM_APPC_NETWORK_CAPABILITY_TYPE_
author: windows-driver-content
description: Specifies the type of app container network capability that is associated with the object or traffic in question.
old-location: fwp\fwpm_appc_network_capability_type.htm
old-project: FWP
ms.assetid: e69ac412-0868-49da-9a87-58a03098839d
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: FWPM_APPC_NETWORK_CAPABILITY_INTERNET_CLIENT, FWPM_APPC_NETWORK_CAPABILITY_INTERNET_CLIENT_SERVER, FWPM_APPC_NETWORK_CAPABILITY_INTERNET_PRIVATE_NETWORK, FWPM_APPC_NETWORK_CAPABILITY_TYPE, FWPM_APPC_NETWORK_CAPABILITY_TYPE enumeration [Filtering], FWPM_APPC_NETWORK_CAPABILITY_TYPE_, fwp.fwpm_appc_network_capability_type, fwpmtypes/FWPM_APPC_NETWORK_CAPABILITY_INTERNET_CLIENT, fwpmtypes/FWPM_APPC_NETWORK_CAPABILITY_INTERNET_CLIENT_SERVER, fwpmtypes/FWPM_APPC_NETWORK_CAPABILITY_INTERNET_PRIVATE_NETWORK, fwpmtypes/FWPM_APPC_NETWORK_CAPABILITY_TYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FWPM_APPC_NETWORK_CAPABILITY_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Fwpmtypes.h
api_name:
-	FWPM_APPC_NETWORK_CAPABILITY_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FWPM_APPC_NETWORK_CAPABILITY_TYPE_ enumeration


## -description


The <b>FWPM_APPC_NETWORK_CAPABILITY_TYPE</b> enumeration specifies the type of app container network capability that is associated with the object or traffic in question.


## -enum-fields




### -field FWPM_APPC_NETWORK_CAPABILITY_INTERNET_CLIENT

Allows the app container to make network requests to servers on the Internet. It acts as a client.


### -field FWPM_APPC_NETWORK_CAPABILITY_INTERNET_CLIENT_SERVER

Allows the app container to make requests and to receive requests to and from the Internet. It acts as a client and also as a server.


### -field FWPM_APPC_NETWORK_CAPABILITY_INTERNET_PRIVATE_NETWORK

Allows the app container to make requests and to receive requests to and from private networks (such as a home network, work network, or the corporate domain network of the computer). It acts as a client and also as a server.


## -see-also




<a href="https://msdn.microsoft.com/39029412-18ce-426a-a79d-cf25ff0dfe0d">Windows Filtering Platform API Enumerated Types</a>
 

 

