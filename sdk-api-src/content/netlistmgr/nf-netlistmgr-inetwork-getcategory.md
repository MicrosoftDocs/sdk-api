---
UID: NF:netlistmgr.INetwork.GetCategory
title: INetwork::GetCategory
author: windows-sdk-content
description: The GetCategory method returns the category of a network.
old-location: nla\inetwork_getcategory.htm
old-project: NLA
ms.assetid: 8a57c6ad-8c6c-4ef0-a731-463a5d7e325f
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetCategory, GetCategory method [Network Awareness], GetCategory method [Network Awareness],INetwork interface, INetwork interface [Network Awareness],GetCategory method, INetwork.GetCategory, INetwork::GetCategory, netlistmgr/INetwork::GetCategory, nla.inetwork_getcategory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: NLM_NETWORK_PROPERTY_CHANGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Netlistmgr.h
api_name:
 - INetwork.GetCategory
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetwork::GetCategory


## -description


The <b>GetCategory</b> method returns the category of a network.


## -parameters




### -param pCategory [out]

Pointer to a <a href="https://msdn.microsoft.com/1bc9720f-7b31-4a09-8bce-a6281ca9b9c4">NLM_NETWORK_CATEGORY</a> enumeration value that specifies the category information for the network.


## -returns



Returns S_OK if the method succeeds.




## -remarks



The private or public network categories must never be used to assume  which Windows Firewall ports are open, as the user can change the default settings of these categories. Instead, Windows Firewall APIs should be called to ensure the ports that the required ports are open.




## -see-also




<a href="https://msdn.microsoft.com/6d483058-f7c4-4a6c-a1a8-816c2fab9994">INetwork</a>



<a href="https://msdn.microsoft.com/1bc9720f-7b31-4a09-8bce-a6281ca9b9c4">NLM_NETWORK_CATEGORY</a>
 

 

