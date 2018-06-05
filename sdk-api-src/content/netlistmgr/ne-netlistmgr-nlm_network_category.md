---
UID: NE:netlistmgr.NLM_NETWORK_CATEGORY
title: NLM_NETWORK_CATEGORY
author: windows-sdk-content
description: The NLM_NETWORK_CATEGORY enumeration is a set of flags that specify the category type of a network.
old-location: nla\nlm_network_category.htm
old-project: NLA
ms.assetid: 1bc9720f-7b31-4a09-8bce-a6281ca9b9c4
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: NLM_NETWORK_CATEGORY, NLM_NETWORK_CATEGORY enumeration [Network Awareness], NLM_NETWORK_CATEGORY_DOMAIN_AUTHENTICATED, NLM_NETWORK_CATEGORY_PRIVATE, NLM_NETWORK_CATEGORY_PUBLIC, netlistmgr/NLM_NETWORK_CATEGORY, netlistmgr/NLM_NETWORK_CATEGORY_DOMAIN_AUTHENTICATED, netlistmgr/NLM_NETWORK_CATEGORY_PRIVATE, netlistmgr/NLM_NETWORK_CATEGORY_PUBLIC, nla.nlm_network_category
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
tech.root: 
req.typenames: NLM_NETWORK_CATEGORY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Netlistmgr.h
api_name:
-	NLM_NETWORK_CATEGORY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# NLM_NETWORK_CATEGORY enumeration


## -description


The NLM_NETWORK_CATEGORY enumeration is  a set of flags that specify the category type of a network.


## -enum-fields




### -field NLM_NETWORK_CATEGORY_PUBLIC

The network is a public (untrusted) network.




### -field NLM_NETWORK_CATEGORY_PRIVATE

The network is a private (trusted) network.




### -field NLM_NETWORK_CATEGORY_DOMAIN_AUTHENTICATED

The network is authenticated against an Active Directory domain.


## -remarks



The private or public network categories must never be used to assume which Windows Firewall ports are open, as the user can change the default settings of these categories. Instead, Firewall APIs should be called to ensure the ports that the required ports are open.



