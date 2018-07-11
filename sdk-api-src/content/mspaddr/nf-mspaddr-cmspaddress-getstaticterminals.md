---
UID: NF:mspaddr.CMSPAddress.GetStaticTerminals
title: CMSPAddress::GetStaticTerminals
author: windows-sdk-content
description: The GetStaticTerminals method is called by our wrapper methods ( get_StaticTerminals and EnumerateStaticTerminals) to get an array of static terminals that can be used on this address.
old-location: tapi3\cmspaddress_getstaticterminals.htm
old-project: tapi
ms.assetid: 8fffc00d-a783-47bc-a081-fe2116060da0
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: CMSPAddress interface [TAPI 2.2],GetStaticTerminals method, CMSPAddress.GetStaticTerminals, CMSPAddress::GetStaticTerminals, GetStaticTerminals, GetStaticTerminals method [TAPI 2.2], GetStaticTerminals method [TAPI 2.2],CMSPAddress interface, _tapi3_cmspaddress_getstaticterminals, mspaddr/CMSPAddress::GetStaticTerminals, tapi3.cmspaddress_getstaticterminals
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mspaddr.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: MSP_EVENT_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mspaddr.h
api_name:
 - CMSPAddress.GetStaticTerminals
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# CMSPAddress::GetStaticTerminals


## -description


The 
<b>GetStaticTerminals</b> method is called by our wrapper methods (
<a href="https://msdn.microsoft.com/f4cdd3f5-ca8c-4660-b37c-c38779a516dd">get_StaticTerminals</a> and 
<a href="https://msdn.microsoft.com/91fea706-9792-40e1-b812-f7578bc7968b">EnumerateStaticTerminals</a>) to get an array of static terminals that can be used on this address. This method updates the address' internal list of terminals by calling 
<a href="https://msdn.microsoft.com/f40964fe-21fe-4dad-8e56-71623ed2be1d">UpdateTerminalList</a> if the list is not up to date. If the <i>ppTerminals</i> parameter is <b>NULL</b> or the *<i>pdwNumTerminals</i> parameter is not large enough to hold all the terminal pointers, this method simply returns (as *<i>pdwNumTerminals</i>) the number of terminals available. If <i>ppTerminals</i> is non-<b>NULL</b> and *<i>pdwNumTerminals</i> is large enough, it <b>AddRefs</b> each terminal pointer and places the array of terminal pointers in *<i>ppTerminals</i>, setting *<i>pdwNumTerminals</i> to the number of terminal pointers returned. If the derived MSP wants to change the set of terminals returned, it will probably override 
<a href="https://msdn.microsoft.com/f40964fe-21fe-4dad-8e56-71623ed2be1d">UpdateTerminalList</a> rather than overriding this method.


## -parameters




### -param pdwNumTerminals [out]

Pointer to number of static terminals.


### -param ppTerminals [out]

Pointer to array of 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interfaces.


## -see-also




<a href="https://msdn.microsoft.com/864bf814-43dd-4d2b-a5a7-fff12520accb">CMSPAddress</a>
 

 

