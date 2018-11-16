---
UID: NF:netlistmgr.INetwork.SetCategory
title: INetwork::SetCategory
author: windows-sdk-content
description: The SetCategory method sets the category of a network. Changes made take effect immediately. Callers of this API must be members of the Administrators group.
old-location: nla\inetwork_setcategory.htm
tech.root: NLA
ms.assetid: 6cbaa23e-f57c-4608-814b-9ccff1ec515f
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: INetwork interface [Network Awareness],SetCategory method, INetwork.SetCategory, INetwork::SetCategory, SetCategory, SetCategory method [Network Awareness], SetCategory method [Network Awareness],INetwork interface, netlistmgr/INetwork::SetCategory, nla.inetwork_setcategory
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Netlistmgr.h
api_name:
 - INetwork.SetCategory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- netlistmgr.h
: 
- INetwork.SetCategory
: 
---

# INetwork::SetCategory


## -description


The <b>SetCategory</b> method sets the category of a network. Changes made take effect immediately. Callers of this API must be members of the Administrators group.


## -parameters




### -param NewCategory [in]

Pointer to a <a href="https://msdn.microsoft.com/1bc9720f-7b31-4a09-8bce-a6281ca9b9c4">NLM_NETWORK_CATEGORY</a> enumeration value that specifies the new category of the network.


## -returns



Returns S_OK if the method succeeds.




## -see-also




<a href="https://msdn.microsoft.com/6d483058-f7c4-4a6c-a1a8-816c2fab9994">INetwork</a>
 

 

