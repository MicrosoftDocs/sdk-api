---
UID: NE:netlistmgr.NLM_DOMAIN_TYPE
title: NLM_DOMAIN_TYPE
author: windows-sdk-content
description: The NLM_DOMAIN_TYPE enumeration is a set of flags that specify the domain type of a network.
old-location: nla\nlm_domain_type.htm
old-project: NLA
ms.assetid: fd1bc50a-c8d3-4594-870e-3bbb5c6ea1da
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: NLM_DOMAIN_TYPE, NLM_DOMAIN_TYPE enumeration [Network Awareness], NLM_DOMAIN_TYPE_DOMAIN_AUTHENTICATED, NLM_DOMAIN_TYPE_DOMAIN_NETWORK, NLM_DOMAIN_TYPE_NON_DOMAIN_NETWORK, netlistmgr/NLM_DOMAIN_TYPE, netlistmgr/NLM_DOMAIN_TYPE_DOMAIN_AUTHENTICATED, netlistmgr/NLM_DOMAIN_TYPE_DOMAIN_NETWORK, netlistmgr/NLM_DOMAIN_TYPE_NON_DOMAIN_NETWORK, nla.nlm_domain_type
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: NLM_DOMAIN_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Netlistmgr.h
api_name:
-	NLM_DOMAIN_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# NLM_DOMAIN_TYPE enumeration


## -description


The NLM_DOMAIN_TYPE enumeration is  a set of flags that specify the domain type of a network.


## -enum-fields




### -field NLM_DOMAIN_TYPE_NON_DOMAIN_NETWORK

The Network is not an Active Directory Network.


### -field NLM_DOMAIN_TYPE_DOMAIN_NETWORK

The Network is an Active Directory Network, but this machine is not authenticated against it.


### -field NLM_DOMAIN_TYPE_DOMAIN_AUTHENTICATED

The Network is an Active Directory Network, and this machine is authenticated against it.

